# Cadaverous Cipher
An uncrackable substitution cipher which uses randomly generated characters as substitutes.

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

## Usage for Shadow Shark Reverse Shell
```
>>> import string
>>> import json
>>> import CadaverousCipher
>>> dictionary = CadaverousCipher.generate_dictionary(string.printable)
>>> dictionary = json.dumps(dictionary)
>>> print(dictionary)
{"0": "\\ud907\\udc3b", "1": "\\ud9c0\\uddc2", "2": "\\ud801\\ude92", "3": "\\ud88f\\udd16", "4": "\\ud8e4\\udc50", "5": "\\ud833\\ude3a", "6": "\\ud8d2\\uddb2", "7": "\\uda27\\udc39", "8": "\\ud8b4\\udd92", "9": "\\ud8c4\\udc11", "a": "\\uda04\\udfd4", "b": "\\uda22\\udf88", "c": "\\uda2b\\udef3", "d": "\\ud9f5\\udd1e", "e": "\\ud912\\udfe0", "f": "\\uda88\\udc4a", "g": "\\uda6b\\udc68", "h": "\\ud98d\\udc6a", "i": "\\udb3e\\udfa3", "j": "\\uda3d\\ude34", "k": "\\ud9d8\\udc62", "l": "\\ud8ba\\udf74", "m": "\\udadf\\udd5e", "n": "\\ud851\\udcdb", "o": "\\ud96b\\ude64", "p": "\\udb58\\uded3", "q": "\\u53a0", "r": "\\ud845\\udc51", "s": "\\udcd2", "t": "\\u32f9", "u": "\\ud94d\\udcc5", "v": "\\ud931\\udd2b", "w": "\\ud8e9\\uddb7", "x": "\\ud9a9\\ude38", "y": "\\ud828\\udf0a", "z": "\\uda16\\udc0a", "A": "\\ud96b\\udc96", "B": "\\ua34e", "C": "\\uda6b\\uddbb", "D": "\\udb10\\udf14", "E": "\\udac4\\udc58", "F": "\\ud8d4\\uddce", "G": "\\udb32\\udd7a", "H": "\\u252e", "I": "\\ud90d\\udcff", "J": "\\ud99b\\udcb3", "K": "\\ud8ce\\udf4f", "L": "\\ud9ef\\udf8e", "M": "\\ud977\\uddcd", "N": "\\ud94d\\ude6f", "O": "\\udb2d\\udd5b", "P": "\\ud939\\udfe0", "Q": "\\ud8a5\\udc06", "R": "\\ud846\\ude12", "S": "\\uda39\\udf36", "T": "\\udb19\\udc01", "U": "\\ud9f4\\uddb0", "V": "\\udaa8\\udfb5", "W": "\\udafe\\udd38", "X": "\\ud887\\udd14", "Y": "\\ud9ba\\ude3c", "Z": "\\udb74\\ude96", "!": "\\udb8a\\udffb", "\\"": "\\ud9ae\\udf3c", "#": "\\ud8d6\\udcb1", "$": "\\ud871\\uddaa", "%": "\\udac9\\udd05", "&": "\\ud892\\udf6d", "\'": "\\ud9e3\\udf9b", "(": "\\uda23\\udf77", ")": "\\udad2\\udc9c", "*": "\\udb0f\\udd39", "+": "\\udb80\\udcf1", ",": "\\udaac\\udf62", "-": "\\ud8a7\\ude25", ".": "\\udb2c\\ude9f", "/": "\\udb57\\uddf7", ":": "\\uc125", ";": "\\uda1a\\udee3", "<": "\\udb65\\udf84", "=": "\\udac8\\udc70", ">": "\\udb53\\uddb6", "?": "\\udb27\\ude5a", "@": "\\uda7c\\uddb6", "[": "\\u6fe4", "\\\\": "\\ud9be\\uddab", "]": "\\ud9f8\\udf98", "^": "\\udb79\\udd92", "_": "\\ud97c\\ude12", "`": "\\udb43\\udf24", "{": "\\ud927\\udd8b", "|": "\\ud92c\\uddd8", "}": "\\ud82e\\udd9f", "~": "\\uda72\\udc0b", " ": "\\udad1\\udf4b", "\\t": "\\uda09\\ude77", "\\n": "\\ud94f\\udc69", "\\r": "\\ud842\\udc51", "\\u000b": "\\udb67\\udfe1", "\\f": "\\ud942\\udff4"}
```
