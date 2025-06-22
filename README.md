# ZhenSharpHelper

[![NuGet](https://img.shields.io/nuget/v/ZhenSharpHelper.svg?style=flat-square)](https://www.nuget.org/packages/ZhenSharpHelper)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

> **A modern utility toolkit for .NET 8+ – Fast, easy, robust.**
---
## ✨ Features Overview

ZhenSharpHelper includes specialized helpers and extension methods for daily .NET development:

### 🅰️ StringHelper
- **Format** (template replace, smart ToString)
- **Split/Join** (delimiter, fixed length, group)
- **Trim, Normalize** (diacritics, accents, unicode, spaces, case)
- **Slugify** (SEO-friendly URL conversion)
- **Parse, Mask** (mask phone/email/card, extract substring, parseInt/parseDouble)
- **Random** (random string, password, guid, number)
- **Regex** (IsMatch, MatchGroup, Replace, Validate, Pattern extractor...)

### 💾 DataHelper
- `ObjectToBytes<T>`, `BytesToObject<T>`
- `StringToBytes`, `BytesToString`
- `BytesToHexString`, `BytesToBase64`, `Base64ToBytes`
- Quick conversion between object, bytes, base64, hex, string
- Data serialization/deserialization helpers

### 🔐 CryptoHelper
- Hash: **MD5, SHA1, SHA256, SHA512, CRC, Bcrypt, ...**
- Encrypt, Decrypt: Symmetric (AES), PasswordHash, Salt
- Random token, guid, hash, etc.

### ✔️ ValidationHelper
- **Email, Phone, Username, Password, CreditCard, ID, Custom pattern**
- Fast IsValidXXX methods for strings and numbers

### 🕑 DateTimeHelper
- Format and parse dates (multiple cultures)
- Convert UTC ↔ Local, any timezone, Unix timestamp
- Date math: Add, Diff, Age, Business day, Range, ...
- TimeZoneInfo, convert timezones, get all system zones

### 📂 FileHelper
- Quick read/write: **XML, Tab, CSV, INI, XLS**
- Path helpers, extension, file size format, secure file ops
- Convert file to base64, hash file, stream tools, more...

### 📦 ZipHelper
- Compress, decompress: **zip, rar, 7z, tar, gz** (auto-detect)
- Extract single/multiple files, password support
---
## ⚡ Quick Start Examples

### 🅰️ StringHelper

```csharp
using ZhenSharpHelper;

// Slugify
string slug = StringHelper.Slugify("Sáng tạo & Đổi mới!"); // "sang-tao-doi-moi"

// Mask
string masked = StringHelper.Mask("0912345678", 3, 3); // "091****678"

// Random password
string pw = StringHelper.RandomString(10);

// Normalize accents
string norm = StringHelper.Normalize("Cà phê sữa đá"); // "Ca phe sua da"
```
### 💾 DataHelper

```csharp
byte[] bytes = DataHelper.StringToBytes("hello world");
string hex = DataHelper.BytesToHexString(bytes);
string b64 = DataHelper.BytesToBase64(bytes);
var obj = DataHelper.BytesToObject<MyClass>(bytes);
```
### 🔐 CryptoHelper

```csharp
string md5 = CryptoHelper.Md5("123456");      // "e10adc3949ba59abbe56e057f20f883e"
string hash = CryptoHelper.Sha256("data");
string encrypted = CryptoHelper.Encrypt("secret", "password123");
string decrypted = CryptoHelper.Decrypt(encrypted, "password123");
```
### ✔️ ValidationHelper

```csharp
bool ok1 = ValidationHelper.IsValidEmail("test@email.com");
bool ok2 = ValidationHelper.IsValidPhone("0912345678");
bool ok3 = ValidationHelper.IsValidUserName("zhen_dev");
```
### 🕑 DateTimeHelper

```csharp
var local = DateTimeHelper.UtcToLocal(DateTime.UtcNow, "SE Asia Standard Time");
var utc = DateTimeHelper.LocalToUtc(DateTime.Now, "SE Asia Standard Time");
string formatted = DateTimeHelper.Format(DateTime.Now, "yyyy-MM-dd HH:mm");
TimeSpan diff = DateTimeHelper.DiffDays(DateTime.Now, DateTime.Now.AddDays(10));
```
### 📂 FileHelper

```csharp
string csv = FileHelper.ReadCsv("data.csv");
FileHelper.WriteXml("data.xml", obj);
string[] lines = FileHelper.ReadTab("data.txt");
```
📦 ZipHelper

```csharp
ZipHelper.CompressFolder("data/", "data.zip");
ZipHelper.Extract("data.zip", "output/", "optionalPassword");
```
---
## 📚 Documentation

- [API Reference (coming soon)](https://github.com/zhenlong-devel/zhensharphelper)
- See code comments (XML doc) and included unit tests for practical usage examples.
- Most methods are named intuitively and easily discoverable via IntelliSense.
- Contributions for improved docs and real-world examples are always welcome at the [GitHub repository](https://github.com/zhenlong-devel/zhensharphelper)!

---
## ❤️ License

This project is licensed under the [MIT License](LICENSE).

© 2025 ZhenGlobal - ZhenLong - zhenlong-devel

---
## 🙌 Contributing
- Pull requests, bug reports and suggestions are welcome!
- Star ⭐ the repo if you find it useful!
---
## 🚀 Installation

```sh
dotnet add package ZhenSharpHelper
```
