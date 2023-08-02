# gpg_tool_for_ctf
The GPG tool, also known as GnuPG (GNU Privacy Guard), is a widely used encryption software that provides cryptographic privacy and authentication for data communication. It is a free and open-source implementation of the OpenPGP (Pretty Good Privacy) standard, which allows users to encrypt and sign data, ensuring its confidentiality and integrity.

To create a key we can follow below process:
1. Install GPG tool on your system.
2. Open the terminal and type `gpg --full-generate-key` command.
3. Follow the prompts to choose the key type, key size, expiration date, and enter your name and email address.
4. Set a passphrase to protect your private key.
5. Your GPG key pair will be generated and stored on your system.

 
For making a file protected with that key we can follow below process:
1. Encrypt the file using the recipient's public key by running the command `gpg --encrypt --recipient <recipient-email> <file-to-encrypt>`. or
2. `gpg -r <key> -e <file name>`
3. The encrypted file will be created with the `.gpg` extension. Share the encrypted file with the recipient.

To decrypt the file we can follow:
1. Import the recipient's private key by running the command `gpg --import <recipient-private-key>`
2. Decrypt the encrypted file by running the command `gpg --decrypt <encrypted-file.gpg>` or `gpg -d <file name>`
3. Enter the passphrase associated with your private key to unlock and decrypt the file.



To save the text to another file:
Simply run the command `gpg -o <output-file-name> -d <encrypted-file.gpg>` or `gpg -o <output-file-name> -d <file name>` to save the decrypted text to a new file.
