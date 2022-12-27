# WeF

Use your web browser to encrypt and decrypt files.
Based on [web-browser-based-file-encryption-decryption](https://github.com/meixler/web-browser-based-file-encryption-decryption) with those changes :

* encryption is done using AES-GCM
* encryption key is derived from the password and a random salt using PBKDF2 derivation with 100000 iterations of SHA-512 hashing
* use a slightly modified dark theme from [simplecss](https://simplecss.org)

## Usage

If runs locally, simply point your web browser to the .html document.

Then, use the web page rendered in your browser to encrypt a file using a password.  Use the same password later to decrypt the file.  IMPORTANT: The same password that was used to encrypt the file must be used to decrypt the file later. If you loose or forget the password, it cannot be recovered!

## Operation and privacy

The page uses javascript running within your web browser to encrypt and decrypt files client-side, in-browser. The page makes no network connections during this process, to ensure that your files and password do not leave your web browser during the process. This can be independently verified by reviewing the source code for the page, or by monitoring your web browser's [networking activity](https://developer.mozilla.org/en-US/docs/Tools/Network_Monitor) during operation of the page. The page can also be downloaded and run locally on your system offline. 

## Verifying the integrity of the files

Here is the expected SHA-256 checksum hash :

    9434fa551fc0be5533965297fd303f10810b9ddc029a16177273ca67a412e52c  index.html
    6d49875145ec16173076685a7158e68be2fdeb8517dfe252d1625b631cb31e29  simple.css

## License

This project is licensed under the [GPL-3.0](https://www.gnu.org/licenses/gpl-3.0.en.html) open source license.