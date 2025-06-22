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

## 🚀 Installation

```sh
dotnet add package ZhenSharpHelper
