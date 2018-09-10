# Signature Value of Created Invoice

Creating method of Signature value：

Step 1、Combination string  
String formation:

```
    {TimeStamp}{Exclusive encryption Salt}
```

Example：  
TimeStamp:1490714051 \(Tue, 28 Mar 2017 15:14:11 GMT\)  
Exclusive encryption Salt provided by e-Invoice: ABCDEFGHIJKLMNOPQRSTUVWXYZ

```
    1490714051ABCDEFGHIJKLMNOPQRSTUVWXYZ
```

Step 2、Use the SHA256 hash with the string

Step 3、Byte\[\] to Hex String

Result of Example：  
    42AFE0433C4EB08B9266E3B50C72A9D11D4946DC79B7AFD4B73AE9175185644B

---

Example for C\#

```cshap
// Get the signature verification value
public string GetInvoiceSignature(string TimeStamp, string Data, string HashSalt)
{
      string _hashString = string.Format("{0}{1}", TimeStamp, HashSalt);
      return SHA256Encrypt(_hashString);
}

// Using SHA256 encryption
public string SHA256Encrypt(string NonEncryptString)
{
    SHA256 sha256 = new SHA256CryptoServiceProvider();//Building SHA256
    byte[] source = Encoding.ASCII.GetBytes(NonEncryptString);//String to Byte[]
    byte[] crypto = sha256.ComputeHash(source);//Encryption with SHA256
    string result = BitConverter.ToString(crypto).Replace("-", string.Empty);//Change the encrypted string from Byte [] to string
    return result;//Output the result
}
```
