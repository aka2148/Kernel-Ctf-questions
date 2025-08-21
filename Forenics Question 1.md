# Title 
Hidden sounds

## Author 
ak2148

## Domain 
Forensics

## Difficulty
Medium-Hardish, im not sure

1. **Zip Archive**
   - Contains **50–100 folders**.
   - Most folders are blocked using steg, except **one openable folder** (easily identifiable).
   - This folder contains an image file.

2. **First Image**
   - Found inside the accessible folder.
   - **Exiftool Analysis** → reveals the name of another file inside the zip (hidden in a field like *comment* or *author*).
         -That file will have the eventual flag.
   - **Binwalk Analysis** → extracts an **audio file** hidden inside the image.

3. **Audio Analysis**
   - The audio encodes the **password** required to open the referenced file.
   - Possible analysis methods:
     - Spectrogram
     - Waveform
     - Morse code
     - Oscilloscope (**preferred**: less commonly known imo)

4. **Password-Protected File**
   - Use the extracted password to open the referenced file.
   - Inside, you’ll find a **final image**.

5. **Final Flag**
   - The image contains the **flag**.

---

## 🧭 Summary of Steps
- Unzip archive → find openable folder.  
- Inspect first image with **Exiftool** and **Binwalk**.  
- Extract hidden audio → analyze using **oscilloscope**.  
- Recover password → open locked file.  
- Obtain final image → extract **flag**.  
