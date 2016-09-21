# information
development information text file

Create ssl localhost 

In mac
step1) npm http-server
step 2) openssl genrsa -des3 -out self-signed.pass.key 2048
step 3) openssl rsa -in self-signed.pass.key -out self-signed.key
step 4) openssl req -new -key self-signed.key -out self-signed.csr
step 5) openssl x509 -req -days 365 -in self-signed.csr -signkey self-signed.key -out self-signed.crt
step 6) echo "SHA1 fingerprint:\n"
step 7) openssl x509 -in self-signed.crt -sha1 -noout -fingerprint
step 8) rm self-signed.pass.key
step 9) rm self-signed.csr
step 10) http-server -S -C /Users/mardesai/Documents/self-signed.crt -K /Users/mardesai/Documents/self-signed.key

In windows 
Step 1) install xampp 
step 2) https://localhost
