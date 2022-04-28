# CadaverousCipher
An uncrackable substitution cipher using randomly generated characters.

## Installation
### Debian
```
$ sudo apt-get install python3 git
$ git clone https://github.com/MrSharkSpamBot/CadaverousCipher.git
```
### Arch
```
$ sudo pacman -S python git
$ git clone https://github.com/MrSharkSpamBot/CadaverousCipher.git
```


## Usage
```
>>> import string
>>> import CadaverousCipher
>>> dictionary = CadaverousCipher.generate_dictionary(string.printable)
>>> dictionary
{'0': '\U000a977f', '1': '\U00041638', '2': '\U000ec795', '3': '\u6859', '4': '\U0004bf55', '5': '\U000cae63', '6': '\U000a6c6f', '7': '\U00095793', '8': '\U00053044', '9': '\U0005a18e', 'a': '\U000ba72a', 'b': '\U000a38e2', 'c': '\U000eb851', 'd': '\U000e8749', 'e': '\U000ba1dc', 'f': '\U000de653', 'g': '\U000c86e8', 'h': '\U0002481d', 'i': '\U0009f2ab', 'j': '\U000673ec', 'k': '\U0007d7d5', 'l': '\U000efb13', 'm': '\U000aa4c6', 'n': '\ub67e', 'o': '\U00020d6e', 'p': '\U00094445', 'q': '\U00063cd4', 'r': '\u2097', 's': '\U0006974a', 't': '\U00098168', 'u': '\U00013030', 'v': '\U000dd0de', 'w': '\U000c5c60', 'x': '\U000c35a9', 'y': '\U0007c54d', 'z': '\u9829', 'A': '\U0006dff9', 'B': '\U0006f41a', 'C': '\U000ad287', 'D': '\U000c4c77', 'E': '\U0006b9e7', 'F': '\U000af636', 'G': '\U000ebc1e', 'H': '\u1386', 'I': '\U000d07f4', 'J': '\U000bef14', 'K': '\U000bd3b9', 'L': '\U000dbaa6', 'M': '\U00065a22', 'N': '\U0008ddf5', 'O': '\U000dc3e2', 'P': '\U000e1fe2', 'Q': '\U0005dfe7', 'R': '\U000d3df3', 'S': '\U000c3a51', 'T': '\U000b5e8f', 'U': '\U0004e074', 'V': '\U000f143e', 'W': '\U000bdaa9', 'X': '\U000e9f88', 'Y': '\U000aadc4', 'Z': '\U000335b0', '!': '\U000e8510', '"': '\u0a84', '#': '\U00034746', '$': '\U000ea007', '%': '\U0003055c', '&': '\U000dfd58', "'": '\U000f3ffa', '(': '\U00063c5e', ')': '\U000822b0', '*': '\U0002e4d6', '+': '\U0001e469', ',': '\U0007880c', '-': '\U00045774', '.': '\U000e8ddc', '/': '\U000882d3', ':': '\U000b1150', ';': '\uf71e', '<': '\U000b4459', '=': '\U0008e77f', '>': '\U000b54fc', '?': '\U00087a46', '@': '\U000f0ae9', '[': '\ua2c1', '\\': '\U000bf09c', ']': '\U00029f95', '^': '\u2dad', '_': '\U00038a77', '`': '\U00085cd8', '{': '\U000db631', '|': '\U0009f2d4', '}': '\U00035841', '~': '\U000da5ee', ' ': '\U00082e3b', '\t': '\U000b0643', '\n': '\U000310f1', '\r': '\U000b43ae', '\x0b': '\U0009c5ba', '\x0c': '\U000acfee'}
>>> encrypted = encrypt('This is the power of the CadaverousCipher...', dictionary)
>>> encrypted
'\U000b5e8f\U0002481d\U0009f2ab\U0006974a\U00082e3b\U0009f2ab\U0006974a\U00082e3b\U00098168\U0002481d\U000ba1dc\U00082e3b\U00094445\U00020d6e\U000c5c60\U000ba1dc\u2097\U00082e3b\U00020d6e\U000de653\U00082e3b\U00098168\U0002481d\U000ba1dc\U00082e3b\U000ad287\U000ba72a\U000e8749\U000ba72a\U000dd0de\U000ba1dc\u2097\U00020d6e\U00013030\U0006974a\U000ad287\U0009f2ab\U00094445\U0002481d\U000ba1dc\u2097\U000e8ddc\U000e8ddc\U000e8ddc'
>>> decrypted = decrypt(encrypted, dictionary)
>>> decrypted
'This is the power of the CadaverousCipher...'
```
