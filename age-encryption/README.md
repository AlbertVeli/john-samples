# age sample files

Sample files for the `age` format in John the Ripper.

[age](https://age-encryption.org/) is a simple, modern file encryption tool.
These samples use passphrase-based encryption (scrypt + ChaCha20-Poly1305).

## Files

| File | Plaintext | Password |
|------|-----------|----------|
| `hello.txt.age` | `Hello, World!` | `iloveyou` |
| `john.txt.age` | `John is so Wonderful!` | `password123` |

## Usage

Extract hashes with `age2john.py`, then crack with john:

```
python age2john.py hello.txt.age john.txt.age > hashes.txt
john hashes.txt
```
