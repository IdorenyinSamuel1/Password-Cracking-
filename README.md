# Password-Cracking-

**Name: Idorenyin Ekopetop Samuel**

**Date: 7/04/2026**

A lab was carried out using John The Ripper to crack password.




**Password Cracking Using John the Ripper (ZIP File) Lab Report**


**Introduction**

Password-protected compressed files are commonly used to secure sensitive data. However, weak passwords can be cracked using password cracking tools. This lab demonstrates how a password-protected ZIP file can be cracked using John the Ripper by extracting the hash and performing a dictionary attack.


**Objective**

Create a password-protected ZIP file
Extract the ZIP hash using zip2john
Crack the password using John the Ripper
Verify the cracked password by extracting the file


**Tools Used**


1. Kali Linux

2. John the Ripper

3. zip2john

4. Terminal

5. Wordlist (custom/common passwords)

**Procedure**

**Step 1:** Create a file


A text file was created on the Desktop.

Bash

echo "This is a password lab file" > secret.txt

**Step 2:** Create password-protected ZIP file

The file was compressed using a common password.


Bash

zip --encrypt secret.zip secret.txt

Password used:

password123


**Step 3:** Extract hash using zip2john

The ZIP file hash was extracted.


Bash

zip2john secret.zip > zip_hash.txt


**Step 4:** Crack password using John the Ripper


John the Ripper was used to crack the ZIP hash.


Bash

john zip_hash.txt

After running, John successfully cracked the password.


**Step 5:** Display cracked password

Bash

john --show zip_hash.txt

Output:

secret.zip:password123

**Step 6:** Verify cracked password


The ZIP file was extracted using the recovered password.

Bash

unzip secret.zip

Password entered:

password123

File successfully extracted:


secret.txt


**Result**

The password-protected ZIP file was successfully cracked using John the Ripper.

The recovered password was:

password123

The ZIP file was successfully extracted using the cracked password.

**Risk Analysis**

1.Weak passwords can be easily cracked

2. Password-protected ZIP files are not fully secure

3. Attackers can extract hashes and perform dictionary attacks

4. Sensitive files protected with weak passwords are vulnerable

**Recommendations**

1. Use strong passwords (uppercase, lowercase, symbols, numbers)

2. Avoid common passwords like "password123"

3. Use AES-256 encryption for sensitive files


4. Implement multi-layer security for confidential data


**Conclusion**

This lab demonstrated how a password-protected ZIP file can be cracked using John the Ripper. The hash extracted using zip2john was subjected to a dictionary attack, and the password was successfully recovered. This shows that weak passwords provide little security and can be easily compromised.


Evidence

<img width="960" height="540" alt="john1" src="https://github.com/user-attachments/assets/c4e7b1ec-d19b-445b-8572-a9b40ad0ae36" />








<img width="960" height="540" alt="john2" src="https://github.com/user-attachments/assets/9f3ec1a3-8fa2-40f3-9f28-78094849da74" />








<img width="960" height="540" alt="john3" src="https://github.com/user-attachments/assets/cfea3b1f-da0f-4540-a5ed-1c555ad4c7a4" />






<img width="960" height="540" alt="john4" src="https://github.com/user-attachments/assets/014ff29c-67cd-477b-b0d5-dc39521c1039" />






<img width="960" height="540" alt="john5" src="https://github.com/user-attachments/assets/c2ebf196-c640-4093-88d2-53313bbb98d0" />





