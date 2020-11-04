# python-password-checker

Securely checks to see if your password has ever been hacked.

If you use a basic online checker you could potentially be giving your password to a hacker. This code cuts out every opportunity a hacker may have to get your password while you are checking to see if it has been hacked.

It pulls your password/s out of a text file which you can later delete. Then it SHA1 hashes your password/s, but since that could also be used to figure out what your password might be, it breaks it into two pieces. Using the first piece (5 characters), it retrieves a list of possible passwords from the pwnedpasswords.com api. It takes that list and finds the matching password/s based on the second piece (the rest of the characters). Finally returning if your password has been found in a hack and how many times it has been breached.

Oh, and if you are running this on your own machine, don't forget to run "pip install requests".
