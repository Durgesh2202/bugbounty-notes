# bugbounty-notes



<h2>Password Reset Poisoning</h2>
Password Reset (Most Critical)
This is the biggest one. Steps:

Go to https://target.net/login.php<br>
Click Forgot Password <br>
Intercept the reset request in Burp<br>
Add X-Forwarded-Host: evil.com<br>
Forward the request<br>
Check if the reset email contains a link pointing to evil.com<br>

If yes → Critical — Password Reset Poisoning
