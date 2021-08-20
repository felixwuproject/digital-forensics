# digital-forensics
Generating an SHA-256 Hash From the Command Line
1. Overview
The SHA-256 standard is used in document integrity checks. It’s preferred over the SHA-1 standard, since the latter has been shown to produce the same hash for different documents.

2. Generate SHA-256 Hashes for Files

In this tutorial, we’ll look at SHA-256 hash generation using the sha256sum command.
echo "https://baeldung.com" > data.txt
sha256sum data.txt 
86c5ceb27e1bf441130299c0209e5f35b88089f62c06b2b09d65772274f12057 data.txt

3. Verify File Integrity
Let’s use the hash stored in the checksum file to verify the integrity of the data.txt file that we’ve hashed:

sha256sum --check checksum
data.txt: OK
