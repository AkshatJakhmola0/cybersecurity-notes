# Observations

## 1. FINDSTR Help (`findstr /?`)

- The help menu displayed the syntax and available options for the FINDSTR command.
- Various search options such as `/i`, `/n`, `/b`, `/c`, and `/r` were available.
- FINDSTR supports both simple text searches and regular expressions.
- The help menu provides a quick reference for advanced text searching.

---

## 2. Basic Search (`findstr "Windows" systeminfo.txt`)

- The command successfully located lines containing the word "Windows".
- Only matching lines were displayed.
- The operating system name and Windows directory were identified.
- The search was case-sensitive by default.

---

## 3. Case-Insensitive Search (`findstr /i "windows" systeminfo.txt`)

- The `/i` option ignored differences in uppercase and lowercase letters.
- Additional matches, including the System Directory, were displayed.
- Case-insensitive searching increases search flexibility.
- This option is useful when the exact letter case is unknown.

---

## 4. Search with Line Numbers (`findstr /n "OS" systeminfo.txt`)

- The `/n` option displayed line numbers before each matching line.
- Multiple operating system-related entries were identified.
- Line numbers made it easier to locate information within the file.
- This feature is useful for log analysis and troubleshooting.

---

## 5. Beginning-of-Line Search (`findstr /b "OS" systeminfo.txt`)

- The `/b` option matched only lines beginning with "OS".
- BIOS information was excluded because it did not start with "OS".
- This option helps narrow search results.
- Beginning-of-line matching improves search accuracy.

---

## 6. Exact Phrase Search (`findstr /c:"Microsoft Windows" systeminfo.txt`)

- The `/c` option searched for the complete phrase as a single string.
- Only the operating system name matched the search phrase.
- Exact phrase searching prevents partial word matching.
- This option is useful when searching for specific text values.

---

## 7. Multiple Keyword Search (`findstr "Memory Version" systeminfo.txt`)

- The command searched for more than one keyword simultaneously.
- Lines containing either "Memory" or "Version" were displayed.
- Windows version, BIOS version, and memory information were retrieved.
- Multiple keyword searches reduce the need for repeated commands.

---

## 8. Regular Expression Search (`findstr /r "^OS" systeminfo.txt`)

- The `/r` option enabled regular expression matching.
- The `^` symbol matched lines starting with "OS".
- All operating system-related entries beginning with "OS" were displayed.
- Regular expressions provide flexible and powerful pattern matching for text analysis.
