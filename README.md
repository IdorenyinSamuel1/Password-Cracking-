# Password-Cracking-



A lab was carried out using John The Ripper to crack password. For education purpose




Password Cracking Using John the Ripper (ZIP File) Lab Report
Introduction
Password-protected compressed files are commonly used to secure sensitive data. However, weak passwords can be cracked using password cracking tools. This lab demonstrates how a password-protected ZIP file can be cracked using John the Ripper by extracting the hash and performing a dictionary attack.
Objective
Create a password-protected ZIP file
Extract the ZIP hash using zip2john
Crack the password using John the Ripper
Verify the cracked password by extracting the file
Tools Used
Kali Linux
John the Ripper
zip2john
Terminal
Wordlist (custom/common passwords)
Procedure
Step 1: Create a file
A text file was created on the Desktop.
Bash
echo "This is a password lab file" > secret.txt
Step 2: Create password-protected ZIP file
The file was compressed using a common password.
Bash
zip --encrypt secret.zip secret.txt
Password used:

password123
Step 3: Extract hash using zip2john
The ZIP file hash was extracted.
Bash
zip2john secret.zip > zip_hash.txt
Step 4: Crack password using John the Ripper
John the Ripper was used to crack the ZIP hash.
Bash
john zip_hash.txt
After running, John successfully cracked the password.
Step 5: Display cracked password
Bash
john --show zip_hash.txt
Output:

secret.zip:password123
Step 6: Verify cracked password
The ZIP file was extracted using the recovered password.
Bash
unzip secret.zip
Password entered:

password123
File successfully extracted:

secret.txt
Result
The password-protected ZIP file was successfully cracked using John the Ripper. The recovered password was:

password123
The ZIP file was successfully extracted using the cracked password.
Risk Analysis
Weak passwords can be easily cracked
Password-protected ZIP files are not fully secure
Attackers can extract hashes and perform dictionary attacks
Sensitive files protected with weak passwords are vulnerable
Recommendations
Use strong passwords (uppercase, lowercase, symbols, numbers)
Avoid common passwords like "password123"
Use AES-256 encryption for sensitive files
Implement multi-layer security for confidential data
Conclusion
This lab demonstrated how a password-protected ZIP file can be cracked using John the Ripper. The hash extracted using zip2john was subjected to a dictionary attack, and the password was successfully recovered. This shows that weak passwords provide little security and can be easily compromised.



