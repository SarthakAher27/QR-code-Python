# QR Code Generator in Python

## Prerequisites
- **Python Version:** 3.10
- **Required Libraries:** qrcode (7.3.1), Pillow (9.2.0)
- **Estimated Read Time:** 40 minutes

---

## Introduction
Have you ever wondered how QR codes work or how procedural images are generated? Do you want to share a website link in a cooler way? If so, this project is for you!

In this tutorial, we will learn how to create a QR code in Python using `qrcode` and `Pillow` in just a few lines of code.

---

## What Is a QR Code?
A QR code (Quick Response code) is a 2D barcode that contains data in black and white patterns. Originally invented in 1994 by a Japanese company, QR codes can store links, text, and other information, accessible simply by scanning with a mobile device.

They are widely used on restaurant menus, business cards, and even advertisements due to their ease of use.

---

## Installation
To install the necessary libraries, run the following command:

```sh
pip install qrcode pillow
```

This tutorial uses:
- `qrcode` version **7.3.1**
- `Pillow` version **9.2.0**

---

## Creating a QR Code
### 1. Setting Up
Create a new Python file (e.g., `qr_code.py`). **Do not name it `qrcode.py`,** as this will conflict with the installed library.

### 2. Writing the Code
Add the following code to generate a QR code for a YouTube video:

```python
import qrcode

website_link = 'https://www.youtube.com/watch?v=dQw4w9WgXcQ'

qr = qrcode.QRCode(version=1, box_size=5, border=5)
qr.add_data(website_link)
qr.make()

img = qr.make_image(fill_color='black', back_color='white')
img.save('youtube_qr.png')
```

### 3. Running the Script
Execute the script using:

```sh
python qr_code.py
```

This will generate a **QR code image (`youtube_qr.png`)** in your project directory.

---

## Understanding the Code
- `QRCode(version=1, box_size=5, border=5)`: 
  - `version`: Controls QR code size (1–40).
  - `box_size`: Specifies the pixel size of each box.
  - `border`: Defines the thickness of the border.
- `qr.add_data(website_link)`: Adds the website link to the QR code.
- `qr.make()`: Generates the QR code.
- `make_image(fill_color='black', back_color='white')`: Creates an image of the QR code.
- `img.save('youtube_qr.png')`: Saves the generated QR code as an image file.

---

## Possible Improvements
- Allow users to **input a website link** dynamically.
- Customize the QR code's **size, color, and border thickness**.
- Generate **multiple QR codes** automatically.
- Add a **GUI interface** using `Tkinter`.
- Experiment with **different colors and styles**.

---

## Additional Resources
- [qrcode Documentation](https://github.com/lincolnloop/python-qrcode)
- [Pillow Documentation](https://pillow.readthedocs.io/en/stable/)
- [Alternative QR Code Library: pyqrcode](https://github.com/mnooner256/pyqrcode)

---

## License
This project is open-source and available under the **MIT License**.

---

Now you're ready to generate your own QR codes! 🚀

