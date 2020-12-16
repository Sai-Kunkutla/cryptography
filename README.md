# cryptography

from cryptography.fernet import Fernet
# Put this somewhere safe!
key = Fernet.generate_key()
f = Fernet(key)
token = f.encrypt(b"A really secret message. Not for prying eyes.")
token
'...'
f.decrypt(token)
'A really secret message. Not for prying eyes.'
