SSH:
- Client generates a pair of public and private key.
- The private key is stored on the machine securely.
- The public key can be shared with the server.
- When the client attempts to connect to the server, the server checks if the client has the public key.
- If the public key matches, the server send encrypted data.
- The client uses the private key to decrypt. The decrypted message is sent back to the server. The server uses the public key to verify.
- If the response matches the expected value, the server authenticate the client.
- Once authenticated, a secure encrypted SSH session is established.
