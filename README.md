QR Code Generator in Python

Prerequisites

Basic knowledge of Python

Python 3.10 installed

Required libraries: qrcode (v7.3.1), Pillow (v9.2.0)

Introduction

This project allows you to generate QR codes in Python using the qrcode library and Pillow. With just a few lines of code, you can create a QR code for any website link and save it as an image.

Installation

Ensure you have Python 3.10 installed, then install the required libraries by running:

pip install qrcode pillow

How to Use

Create a new Python file, e.g., qr_code.py.

Add the following code to generate a QR code:

import qrcode

website_link = 'https://www.youtube.com/watch?v=dQw4w9WgXcQ'

qr = qrcode.QRCode(version=1, box_size=5, border=5)
qr.add_data(website_link)
qr.make()

img = qr.make_image(fill_color='black', back_color='white')
img.save('youtube_qr.png')

Run the script:

python qr_code.py

A QR code image (youtube_qr.png) will be saved in your project directory.

Features

Generate QR codes quickly and efficiently.

Customize the QR code's version, size, and border.

Save the QR code as an image file.

Potential Improvements

Accept website links from user input.

Allow customization of QR code parameters.

Generate multiple QR codes automatically.

Implement a GUI using Tkinter.

Experiment with different colors and styles.

Resources

qrcode Documentation

Pillow Documentation

License

This project is open-source and available for use under the MIT License.
