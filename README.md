# SteganoVault | Hide Secrets in Pixels
-> SteganoVault is a lightweight, browser-based cybersecurity tool that implements Least Significant Bit (LSB) Steganography. It allows users to embed secret text messages within image pixels such that the change is invisible to the human eye.

 How it Works (The Technical Logic)
-> Digital images are made of pixels, and each pixel is composed of RGBA (Red, Green, Blue, Alpha) channels. Each channel is represented by 8 bits (0-255).

Binary Conversion: The secret message is first converted into an 8-bit binary string.

LSB Manipulation: The algorithm targets the Red channel of each pixel. It replaces the Least Significant Bit (the 8th bit) with one bit of the secret message.

Invisibility: Since the 8th bit only changes the color value by 1 (e.g., from 255 to 254), the visual difference is mathematically present but biologically impossible for a human to detect.

Extraction: The decoder reads the LSB of each pixel sequentially and reconstructs the binary string back into readable text until it hits the special "terminator" string (###).

Features
-> Zero Distortion: Hide data without affecting the image quality or aesthetics.
-> Pure JavaScript: No heavy libraries or backend required. Works entirely on the client side using HTML5 Canvas API.
-> Secure Handling: Uses a custom terminator signature to ensure data integrity during extraction.
-> User-Friendly UI: Modern, dark-themed "Hacker" aesthetic for an immersive experience.

Tech Stack
-> Frontend: HTML5, CSS3 (Custom Properties & Grid)
-> Logic: Vanilla JavaScript (ES6+)
-> Processing: Canvas API for direct pixel manipulation

📖 How to Use
Encode:
-> Upload any .png image (Lossless formats work best).
-> Type your secret message in the input box.
-> Click "Generate Secret Image".
-> Right-click and save the generated image.

Decode:
-> Upload the encoded image.
-> Click "Reveal Message".
-> Your hidden secret will appear magically!

👨‍💻 About the Developer
I am a 1st-year Engineering Student passionate about Cybersecurity, Image Processing, and Web Technologies. This project was built to explore how data can be manipulated at the bit level within digital media.
