# Week 3: Password Cracking with John the Ripper & Networkwalks Tools

## 📌 Project Overview
This repository documents the successful completion of **Project Module 1 & 2: Password Cracking**. The objective was to recover the password of a protected PDF file (`My Locked PDF1.pdf`) using two distinct methodologies:
1. **John the Ripper (Johnny GUI)** on a Windows environment.
2. **Networkwalks Online Tools** (Hash Calculator & Password Cracker).

## 🎯 Objectives
* Extract the cryptographic hash (`$pdf$...`) from an encrypted PDF.
* Utilize John the Ripper to perform a dictionary/brute-force attack to crack the hash.
* Utilize Networkwalks web-based tools to achieve the same result via a browser.
* Access the encrypted PDF to retrieve the hidden flag.

## 🛠️ Tools Used
* **OS:** Windows
* **Tool 1:** John the Ripper (Jumbo version) & Johnny GUI
* **Tool 2:** [Networkwalks Hash Calculator](https://networkwalks.com/hash-calculator/)
* **Tool 3:** [Networkwalks Password Cracker](https://networkwalks.com/password-cracker/)

---

## 🚀 Lab Execution & Walkthrough

### Phase 1: Cracking with John the Ripper (Johnny GUI)
1. **Hash Extraction:** Extracted the PDF hash and saved it to a text file named `hash.txt` using Notepad.
2. **Setup:** Configured Johnny to point to the correct `john.exe` executable in the run folder.
3. **Execution:** Loaded `hash.txt` into Johnny and initiated the attack.
4. **Result:** Successfully cracked the password: `password1`.

![Saving the Hash File](screenshots/01_saving_hash_txt.png)
*Figure 1: Saving the extracted PDF hash to hash.txt*

![Johnny Settings](screenshots/02_johnny_settings.png)
*Figure 2: Configuring Johnny GUI with the John the Ripper executable*

![Johnny Loaded Hash](screenshots/03_johnny_loaded_hash.png)
*Figure 3: Loading the hash file into Johnny*

![Johnny Cracked](screenshots/04_johnny_cracked_password.png)
*Figure 4: Johnny successfully cracking the hash (password1)*

---

### Phase 2: Cracking with Networkwalks Online Tools
1. **Web Hash Calculator:** Uploaded the encrypted PDF to the Networkwalks Hash Calculator to extract the `$pdf$` hash.
2. **Web Password Cracker:** Pasted the hash into the Password Cracker tool.
3. **Result:** The tool successfully matched the hash and revealed the password: `password1`.

![Networkwalks Hash Calculator](screenshots/06_networkwalks_hash_calculator.png)
*Figure 5: Extracting the PDF hash using the Networkwalks Hash Calculator*

![Networkwalks Password Cracker](screenshots/07_networkwalks_password_cracker.png)
*Figure 6: Cracking the hash using the Networkwalks Password Cracker*

---

### Phase 3: Verification & Flag Capture
Using the cracked password (`password1`), the PDF was successfully decrypted, revealing the final flag.

![PDF Unlocked](screenshots/05_pdf_unlocked.png)
*Figure 7: Entering the cracked password to unlock the PDF*

![Flag Captured](screenshots/08_flag_captured.png)
*Figure 8: The final flag revealed inside the decrypted PDF*

**🏁 Flag:** `nwnetworkwalks_flag1_JR_270521_1`

---

## 🧠 Key Takeaways
* **Hash Extraction:** Password-protected documents store their passwords as cryptographic hashes, not plain text. Extracting these hashes is the first step in recovery.
* **Why Strong Passwords Matter:** The password `password1` was cracked in seconds because it is a common dictionary word with a standard suffix. Stronger passwords (long, complex, random) take significantly longer to crack.
* **Tool Diversity:** While CLI/GUI tools like John the Ripper are incredibly powerful for offline cracking, web-based tools like Networkwalks offer accessible, browser-based alternatives for quick extractions.
