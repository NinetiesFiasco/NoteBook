Шифровальня
-

## C# 
#### `using System.Text;` 
`Encoding.UTF8.GetBytes(str)` - Получить массив байтов из строки  
`Encoding.UTF8.GetString(buffer)` - Получить строку из  массива байтов  

`Convert.ToBase64String(buffer)` - Получить base64 строку из массива байтов  
`Convert.FromBase64String(buffer)` - Получить массив байтов из base64 строки

## получить md5 хэш
#### `using System.Security.Cryptography;`
```
byte[] hash = Encoding.UTF8.GetBytes(str);    
MD5 md = MD5.Create();  
byte[] buff = md5.ComputeHash(hash);  
string result = "";  
foreach (byte b in buff){  
  result += b.ToString("x2")  
}  
```
