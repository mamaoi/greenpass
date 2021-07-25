# Green Pass Verifier

Scriptable green pass verifier.
With this application you can automatize accesses based on green pass validity.

## Installation
<!--
You can just install the application using pip:
```bash
$ pip3 install greenpass
```
-->

If you want to install it from sources, install the python3 requirements
using the following command:
```bash
$ pip3 install -r requirements.txt
```

## Usage
You can feed the application with different file formats, for instance:

Green pass official PDFs
```bash
$ greenpass --pdf greenpass.pdf
```

QRCode images in PNG
```bash
$ greenpass --qr greenpass.png
```

Txt files with the content of the qrcode
```bash
$ greenpass --txt greenpass.txt
```

Standard input and pipes
```bash
$ zbarimg --raw greenpass.png | greenpass --txt -
```

The application returns an UNIX compatible code, therefore you can concatenate commands that will be executed only if the green pass is verified
```bash
$ greenpass --qr greenpass.png && echo "green pass ok"
```
