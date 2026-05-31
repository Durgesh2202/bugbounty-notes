# bugbounty-notes

Password Reset Poisoning
Password Reset (Most Critical)
This is the biggest one. Steps:

Go to https://target.net/login.php
Click Forgot Password
Intercept the reset request in Burp
Add X-Forwarded-Host: evil.com
Forward the request
Check if the reset email contains a link pointing to evil.com

If yes → Critical — Password Reset Poisoning
