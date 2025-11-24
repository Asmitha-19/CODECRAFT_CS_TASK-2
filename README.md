🔐 Image Encryption Tool (Swap + XOR)

A lightweight and powerful image encryption & decryption tool built using Python, supporting:

XOR Encryption / Decryption

Pixel Swap Encryption

Pixel Swap Decryption

Combined Encryption (Swap → XOR)

Combined Decryption (XOR → Swap)

Works with or without NumPy

Supports any RGB image

📌 Features
1. XOR Encryption

Fast bitwise XOR applied to each pixel.

Works with a key range from 0 to 255.

Reversible using the same key.

2. Pixel Swap Encryption

Pixels are shuffled using a random seed.

Same seed is required to decrypt.

Adds strong permutation-based security.

3. Combined Encryption

Performs Swap → XOR, providing:

Pixel position scrambling

Pixel value scrambling

Much stronger than simple XOR or Swap alone.

4. Automatic NumPy Acceleration

If NumPy is available:

Encryption becomes 10x faster

Otherwise falls back to pure Python mode.

📦 Installation
1. Install Dependencies
pip install pillow numpy


NumPy is optional — the script works even without it.

2. Clone This Repository
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>

▶️ Running the Program

Run:

python image_encryptor.py


You will see this menu:

=== Powerful Image Encryption Tool (Swap + XOR) ===

Menu:
1. XOR Encrypt/Decrypt
2. Swap Encrypt
3. Swap Decrypt
4. Combined Encrypt (Swap → XOR)
5. Combined Decrypt (XOR → Swap)
6. Exit

🛠 How It Works
XOR Transformation

Each pixel (R,G,B) is XORed with a key:

r ^ key, g ^ key, b ^ key

Swap Encryption

Converts image into a pixel list

Shuffles using pseudo-random generator with a seed

Stores encrypted image

Swap Decryption

Uses same seed to reverse shuffle order

Correctly restores original pixel arrangement

Combined Encryption
Input Image
   ↓
Swap Encrypt
   ↓
XOR Encrypt
   ↓
Final Encrypted Image

Combined Decryption

Reverse order:

Encrypted Image
   ↓
XOR Decrypt
   ↓
Swap Decrypt
   ↓
Original Image Restored

📁 Project Structure
image-encryption/
│
├── image_encryptor.py      # Main program
├── README.md               # Documentation
└── sample.jpg              # Example input (optional)

⚠️ Security Notes

This is not military-grade encryption.

Intended only for learning, research, and educational purposes.

Do not use for hiding sensitive or personal data.

Always respect ethical and legal guidelines.

🤝 Contributing

Pull requests, feature improvements, and bug fixes are welcome!

🏆 Author

C Asmitha 
This project was created as part of academic and training tasks focusing on cryptography basics.

📜 License

This project is released under the MIT License.

