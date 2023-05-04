Download Link: https://assignmentchef.com/product/solved-csci301-assignment1-creating-ransomware
<br>
<u>In this assignment, your task is to write a simple ransomware using Python</u> <u>script with the</u> <strong><u>pycryptodome</u></strong><u> package.</u>

The assumptions on the ransomware are as follows: 1) An attacker has already broken into a victim’s Linux/Unix machine on which <strong>Python 3.5 or above</strong> and <strong>pycryptodome</strong> package are installed; 2) the attacker put its ransomware program, which is not necessary to be a single file, in the victim’s machine; 3) the victim has three to four text files and a python file in the directory where ransomware locates. Note that the text files have extension “.txt” and the python file has extension “.pye”.

The ransomware should perform the following:

<ul>

 <li>It generates a 256 bits random key for symmetric encryption using AES_CBC.</li>

 <li>It encrypts <strong>all </strong><strong>.txt files</strong> to <strong>.</strong><strong>enc</strong> <strong>files</strong> in the current directory using the key that the attacker generated in step 1). The files in the other folders or the files in the same folder but having different file extensions must not be impacted by the ransomware.</li>

 <li>It comments out all the content of the existing <strong>.</strong><strong>pye</strong> file in the target folder (do not delete the content) and replicates itself to the <strong>.</strong><strong>pye file</strong> for the further propagation.</li>

 <li>The key in step 1) is encrypted to bin using public key encryption.</li>

 <li>It will finally display a message for asking ransom “Your text files are encrypted. To decrypt them, you need to pay me $5,000 and send bin in your folder to [me].” “[me]” should be your student email address.</li>

</ul>

Other requirements:

<ul>

 <li>In step 1), the key used to encrypt files must not appear in the source code of the ransomware program and must not be stored in the plaintext format in the victim’s system.</li>

 <li>All <strong>.txt</strong> files locating in the folder where ransomware program is located must be deleted after they are encrypted to the <strong>.</strong><strong>enc</strong></li>

 <li>AES_CBC mode needs an initial vector (IV) for encryption and decryption. You can fix (i.e., hard-code) this parameter in your ransomware.</li>

 <li>You must use <strong><em>pycryptodome</em></strong> for AES and public key encryption.</li>

 <li>The infected <strong>.</strong><strong>pye file</strong> in step 3) shares the public key of your original ransomware.</li>

</ul>

<u>Your next task is to write programs, key-recovery and file-recovery programs</u> <u>that recover</u> <u>(decrypt) all the encrypted files if the victim pays the ransom.</u>




<ul>

 <li>The key-recovery program decrypt the encrypted key</li>

</ul>

(key.bin) and encode the decrypted key to base64 and store it in key.txt.

<ul>

 <li>The file-recovery program must allow a user to decrypt the encrypted files created in step 2) using the key file created in 6). You do not need to recover the infected <strong>.</strong><strong>pye file</strong> in step 3).</li>

</ul>


