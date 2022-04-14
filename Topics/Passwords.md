# Passwords :closed_lock_with_key:

Passwords are essential to securing your accounts and protecting your data. But what
differentiates a secure from an unsecure password for your accounts?

Here is a nice illustration, which i got recommendad multiple times and you may know too, about the strenght of 
passwords:

<a href="https://xkcd.com/936/" target="_blank"><img src="https://imgs.xkcd.com/comics/password_strength.png" 
alt="Buy Me A Coffee" height="100%" width="80%"></a>

Traditional password policies used to recommend something like this:
- minimum 8 characters
- 3 out of 4 complexity criteria:
    - lowercase
    - uppercase
    - number
    - symbol
- Change every 90 days

The problem with this policies are, that these will create weak passwords through the constant need to change the
password and will perhaps create passwords like this: `Spring2022` 
The password has a fixed format and is easy to break for an attacker with an brute force attack or an dictionary attack.

The only part, which slows a hacker down, who is trying to crack your password hash is the length of your password. In fact it can slow an attacker so much down that the ROI is negative and the attacker will eventually just give up 
cracking the password.
