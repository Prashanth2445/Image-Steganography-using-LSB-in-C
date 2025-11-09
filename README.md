# Image-Steganography-using-LSB-in-C
This project implements Image Steganography using the Least Significant Bit (LSB) technique. The goal is to hide a secret message file inside a .BMP image without changing how the image looks visually.  Steganography helps to securely conceal information inside media, making the communication undetectable.
#✨ Features

🔐 Encode secret text into a .bmp image

🔓 Decode the hidden message back safely

🎨 Uses the Least Significant Bit method for minimal visual distortion

📁 Supports 24-bit BMP image format

🚀 Command-line based, fast, lightweight implementation

✅ Handles errors like invalid files, insufficient image size, etc.

🧠 How It Works

A pixel contains 3 color components: R, G, and B.

Each component is stored in 8 bits:

Example Byte: 11001010
                ↑
               LSB (modified to store hidden message bits)


By changing only the last bit, image quality remains visually the same, but it now carries secret data.

📂 Project Structure
├── main.c
├── encode.c
├── decode.c
├── encode.h
├── decode.h
├── types.h
├── Makefile
├── input_image.bmp
├── secret.txt
└── stego_output.bmp

⚙️ Compilation
make


If Makefile not provided:

gcc main.c encode.c decode.c -o lsb_steg

▶️ Usage
Encoding
./lsb_steg -e <input_image.bmp> <secret.txt> <output_image.bmp>


Example:

./lsb_steg -e beautiful.bmp secret.txt stego_img.bmp

Decoding
./lsb_steg -d <stego_image.bmp> <output_file.txt>


Example:

./lsb_steg -d stego_img.bmp decoded.txt

🔧 Requirements

GCC Compiler

Linux / Windows

24-bit BMP image

💡 Skills Demonstrated

Bitwise operations

File handling (binary mode)

BMP image format handling

Modular programming in C

Debugging & CLI tool creation

📜 License

This project is released under the MIT License.
Feel free to use, modify, and learn from it 🚀

🤝 Contributions

Pull requests are welcome!
For major changes, please open an issue first to discuss ideas.
