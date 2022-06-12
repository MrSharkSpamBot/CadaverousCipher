# Cadaverous Cipher
A polyalphabetic substitution cipher which uses randomly generated characters as substitutes.

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
{1: {'0': '\U000c6739', '1': '\U000b25be', '2': '\U00093bbb', '3': '\U000c763d', '4': '\U00096b3c', '5': '\U00065f33', '6': '\U0007468a', '7': 'व', '8': '\U00042827', '9': '\U000551ed', 'a': '\U00079e06', 'b': '\U000e3342', 'c': '𫾏', 'd': '\U000310aa', 'e': '\U000d03f0', 'f': '\U000d05ce', 'g': '\U000f23d0', 'h': '\U0007265e', 'i': '\U00098452', 'j': '\U000499a6', 'k': '\U00089764', 'l': '\U000bc27e', 'm': '\U000628f7', 'n': '\U0009a664', 'o': '\U000461f9', 'p': '\U0009205a', 'q': '\U000ac825', 'r': '\U000c78f7', 's': '\U000e84e6', 't': '\U000b0a93', 'u': '\U0005812b', 'v': '\U000cc0f8', 'w': '\U000d2a14', 'x': '\U000695ec', 'y': '𝜸', 'z': '\U000b5214', 'A': '\U000509c9', 'B': '\U0004fb84' , 'C': '嘮', 'D': '\U0008acb2', 'E': '𧎕', 'F': '𦗈', 'G': '\U00044f4b', 'H': '閲', 'I': '\U000c6a83', 'J': '\U0007ac03', 'K': '\U000a4617', 'L': '\U00087f32', 'M': '\U000646da', 'N': '\U00053a7b', 'O': '\U0009552b', 'P': '\U000815b7', 'Q': '\U000c24a7', 'R': '\U0005414f', 'S': '\U000c6a6e', 'T': '𩾌', 'U': '\U000546c8', 'V': '\U000a0f47', 'W': '\U000cd929', 'X': '\U0008b364', 'Y': '\U00031a10', 'Z': '\U0005b6f8', '!': '\U0008a5b4', '"': '\U000b48b5', '#': '\U00019f0f', '$': '\U000a5a7e', '%': '\U000b463b', '&': '\U0003e86c', "'": '\U0006feb9', '(': '\U0009e8a2', ')': '\U0004a9ff', '*': '\U0007cec9', '+': '\U000ecb86', ',': '𦘱', '-': '\U0009161a', '.': '\U000b084e', '/': '\U000552cf', ':': '\U0003ccf8', ';': '\U000b6d9c', '<': '\U000e0dfa', '=': '\U000bb238', '>': '𔓜', '?': '\U000dd963', '@': '\U00098c5c', '[': '\U0005dfcf', ' \\': '\U00018b46', ']': '\U00077ff9', '^': '涝', '_': '\U0006632d', '`': '\U000c765f', '{': '\U0009cb37', '|': '\U000efacc', '}': '\U000a61e0', '~': '\U00048ae3', ' ': '䯥', '\t': '\U0005e1b1', '\n': '\U000ae8f0', '\r': '\U000d7ce9', '\x0b': '\U000e890d', '\x0c': '\U0008fc20'}, 2: {'0': '\U0001aaac', '1': '\U00086b04', '2': '\U0001a9be', '3': '\U000305ab', '4': '\U0004d00a', '5': '\U0004fa7f', '6': '\U000c0f63', '7': '\U000edf2b', '8': '\U0004b3dd', '9': '摵', 'a': '\U0005b756', 'b': '\U00014b5e', 'c': '\U0002f5fa', 'd': '\U000e1b64', 'e': '\U00042c95', 'f': '\U000a14a4', 'g': '\U000306fe', 'h': '\U000dc301', 'i': '\U000c0cc5', 'j': '\U000c9830', 'k': '\U00098b5a', 'l': '\U0003fade', 'm': '\U0005a098', 'n': 'ᒤ', 'o': '𬭇', 'p': '\U000aa5b0', 'q': '\U00045f13', 'r': '\U000978d1', 's': '\U0004d34c', 't': '\U00057424', 'u': '\U000ac4ce', 'v': '\U00019b0d', 'w': '\U00096e72', 'x': '\U0008aec7', 'y': '\U000783dc', 'z': '\U000665b3', 'A': '\U000756b9', 'B': '\U000ab8b6', 'C': '\ued9a', 'D': '\U000a8ccc', 'E': '\U000c367d', 'F': '鍌', 'G': '\U0004845a', 'H': '\U000d5cb1', 'I': '匼', 'J': '\U0004168a', 'K': '鐫', 'L': '\u12b7', 'M': '𮮫', 'N': '緇', 'O': '\U000b4a65', 'P': '\U0004c0eb', 'Q': '\U000c2b4e', 'R': '媭', 'S': '\U000373f5', 'T': '\U00014ab5', 'U': '\U000a1864', 'V': '\U000a49a6', 'W': '𬒄', 'X': '夏', 'Y': '𔒎', 'Z'
: '\U000d9722', '!': '\U000e132a', '"': '印', '#': '\U000b69af', '$': '\U000b6717', '%': '𭡍', '&': '\U00044ecb', "'": '\U000a3b3b', '(': '\U0009f059', ')': '𭻡', '*': '\U0001255b', '+': '\U00046ace', ',': '\U000a0f83', '-': '\U000734e2', '.': '\U000edf49', '/': '\U000eaea3', ':': '\U0009ed95', ';': '\U0004c1b5', '<': '\U000c12de', '=': '\U000ecbe6', '>': '�'', '?': '\U000309da', '@': '\U00046bd9', '[': '꧘', '\\': '\U0006538f', ']': '\U0006bda5', '^': '\U000d5c3c', '_': '\U000dd90a', '`': '\U000a6235', '{': '𛰋', '|': '\U000eac57', '}': '\U000e32a3', '~': '\U00051475', ' ':  '\U0001ea90', '\t': '\U0006f78c', '\n': '\U000c9232', '\r': '\U00087db9', '\x0b': '\U0008451e', '\x0c': 'ꦗ'}}
>>> encrypted = CadaverousCipher.encrypt('This is the power of the CadaverousCipher...', dictionary)
>>> encrypted
'\U00014ab5\U0007265e\U000c0cc5\U000e84e6\U0001ea90\U00098452\U0004d34c䯥\U00057424\U0007265e\U00042c95䯥\U000aa5b0\U000461f9\U00096e72\U000d03f0\U000978d1䯥𬭇\U000d05ce\U0001ea90\U000b0a93\U000dc301\U000d03f0\U0001ea90嘮\U0005b756\U000310aa\U0005b756\U000cc0f8\U00042c95\U000c78f7𬭇\U0005812b\U0004d34c嘮\U000c0cc5\U0009205a\U000dc301\U000d03f0\U000978d1\U000b084e\U000edf49\U000b084e'
>>> decrypted = CadaverousCipher.decrypt(encrypted, dictionary)
>>> decrypted
'This is the power of the CadaverousCipher...'
```
