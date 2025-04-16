
# zipCracker - Automatic ZIP Password Cracker using John the Ripper

zipCracker is a Python script that automates the process of cracking password-protected ZIP files using [John the Ripper](https://www.openwall.com/john/).

## 🔧 Requirements

- `zip2john` and `john` must be installed and available in your system's `PATH`.
- You can get the latest John the Ripper (Jumbo version) from the official GitHub:  
  👉 https://github.com/openwall/john

## 🚀 How It Works

1. You input the path to a ZIP file.
2. The script uses `zip2john` to extract the hash.
3. You choose an **incremental mode**.
4. `john` starts cracking the password automatically.
5. The script prints the cracked password directly (no need to run `john --show` manually).

## 🧠 Incremental Modes Explained

When cracking with `--incremental=MODE`, John uses custom character sets and brute-force logic. Here are the available modes:

| Mode     | Description                                      |
|----------|--------------------------------------------------|
| **All**  | All printable characters (letters, numbers, symbols) |
| **Digits** | Numbers only (`0-9`)                          |
| **Alpha** | Alphabet letters (`a-z`, `A-Z`)                 |
| **Lower** | Lowercase letters only (`a-z`)                 |
| **Upper** | Uppercase letters only (`A-Z`)                 |
| **Alnum** | Letters + numbers (`a-z`, `A-Z`, `0-9`)        |

## 💻 Usage Example

```bash
python main.py
```

Then follow the prompts:  
- Enter ZIP path  
- Enter output hash path  
- Choose cracking mode

## 📦 Output Example

```
✅ Password found:
wasabi
```

## ❗ Note

If you interrupt the cracking process, John will save a session file and you can resume it with:

```bash
john --restore
```
## 🔑 KEY
Get the access key [here](https://sfl.gl/LODVkrZ) 

# Happy cracking 😈
