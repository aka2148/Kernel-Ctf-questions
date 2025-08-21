# Title
The Key is Rotation

## Author
your_ctf_name

## Domain
Cryptography

## Difficulty
Medium

### Question Description
You are given two encrypted strings. One of them hides the actual flag, but each character has been rotated by a *different amount*. The second encrypted string reveals the rotation values — but it is encrypted itself.  

Hints:  
- All rotations are under 26.  
- One rotation is exactly 26, hinting that the method is a rotation cipher.  
- The second cipher uses a simple classical cipher.  

**Provided:** Two cipher texts  

### Intended Solution
1. **Step 1: Decrypt the shift cipher**  
   - The second cipher is encoded with a Vigenère cipher.  
   - The challenge title ("The Key is Blank") suggests that the Vigenère key is `"blank"`.  (I'd like to make it the key is rotation.)
   - After decryption, the result looks like:  
     ```
     2_12_3_18_5_26_...
     ```  
   - These numbers represent the per-character rotation values.

2. **Step 2: Decrypt the ROT cipher**  
   - The first cipher text looks like random letters, for example:  
     ```
     abihbhjlkhfryobv467
     ```  
   - Apply the rotation values from step 1 *character by character*.  
   - Each character is shifted backwards by the corresponding number.  
   - When done correctly, this reveals the plaintext:  
     ```
     
     ```

### Flag
> 
