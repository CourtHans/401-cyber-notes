# Day 6 - Data file encryption
10/12/20

* [Applying The CIA Triad To Your Enterprise File Transfer](https://www.jscape.com/blog/implementing-the-cia-triad-when-transferring-files-through-the-internet)
* [What Are MD5, SHA-1, and SHA-256 Hashes, and How Do I Check Them?](https://www.howtogeek.com/67241/htg-explains-what-are-md5-sha-1-hashes-and-how-do-i-check-them/)

***Confidentiality***
In the context of information security, confidentiality refers to the principle of restricting access to or knowledge of certain pieces of information to certain individuals.

***Integrity***
Data integrity pertains to the principle of preventing data from being tampered with.

***Availability***
Ensuring your data is accessible to you (and other authorized access users) at all times.

**Popular methods for securing file transfer confidentiality**</br>
Encryption - data-at-rest and data-in-transit</br>
File transfers need both - end-to-end encryption

Data-in-transit encryption is usually achieved via SSL (e.g. FTPS, HTTPS, WebDAVs) or SSH (e.g. SFTP)

Another method is authentication (i.e. 2F or MF authentication)

*Integrity* - "To achieve data integrity in your file transfers, you can use hash functions and digital signatures, security elements that are readily available in secure file transfer protocols like FTPS, HTTPS, SFTP, and WebDAVs. These solutions will enable file transfer recipients to determine if the files they receive have been tampered along the way."

*Availability* - "The best way to ensure (file transfer) service availability is to set up a high availability (HA) cluster. There are two ways to do this. The first one would entail setting up one or more failover server(s) that can immediately take over should the primary server go down. This is known as an active-passive high availability configuration."

The best solution is to find a single solution that already incorporates all three elements.

### MD5, SHA-1, and SHA-256 hashes

"Software creators often take a file download—like a Linux .iso file, or even a Windows .exe file—and run it through a hash function. They then offer an official list of the hashes on their websites. That way, you can download the file and then run the hash function to confirm you have the real, original file and that it hasn’t been corrupted during the download process."

This is an excellent way to check the validity of files gotten from unofficial sources...try to use SHA-256 whenever possible. 

Hashes should always be identical if using the same hash function on the same file.

  To get the hash file in Powershell:</br>
`Get-FileHash C:\path\to\file.iso`</br>
(replacing C:\path\to\file.iso with your file path). The default will be SHA-256</br>
You can change it by specifying a different hashing algorithm:</br>
```
Get-FileHash C:\path\to\file.iso -Algorithm MD5
Get-FileHash C:\path\to\file.iso -Algorithm SHA1
Get-FileHash C:\path\to\file.iso -Algorithm SHA256
Get-FileHash C:\path\to\file.iso -Algorithm SHA384
Get-FileHash C:\path\to\file.iso -Algorithm SHA512
Get-FileHash C:\path\to\file.iso -Algorithm MACTripleDES
Get-FileHash C:\path\to\file.iso -Algorithm RIPEMD160
```
On a Mac OS, your options are:</br>
```
md5 /path/to/file
shasum /path/to/file
shasum -a 256 /path/to/file
```
On Linux:</br>
```
md5sum /path/to/file
sha1sum /path/to/file
sha256sum /path/to/file
```
Verify the cryptographic signature!
