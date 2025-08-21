# Title
Hidden in Plain Sight

## Author
your_ctf_name

## Domain
Digital Forensics

## Difficulty
Easy-Medium

### Question Description
You are given a raw disk image file (`hidden_photos.dd`). The disk once contained some deleted images. Recover the files and find the real hidden secret.  

**Provided:** `hidden_photos.dd`

### Intended Solution
1. Use **TestDisk** to recover deleted files from the disk image. One newimages will be found:  
   - It is a normal photo (red herring).  
  

2. Inspect the suspicious image with a tool like `binwalk` or `strings`. You’ll notice that another image is hidden **after the end of file marker (EOF)** inside the same file.  

3. Extract the hidden image:  
   - Run `binwalk -e suspicious.jpg` to automatically extract it, or  
   - Manually carve out the second image starting from its `FF D8` (JPEG header).  

4. Open the extracted hidden image to reveal the flag.  

### Flag
> Give Flag here?
