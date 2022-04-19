# Passwords :closed_lock_with_key:

Passwords are essential to securing your accounts and protecting your data. But what
differentiates a secure from an unsecure password for your accounts?

Here is a nice illustration, which i got recommendad multiple times and you may seen too, about the strenght of 
passwords:

<a href="https://xkcd.com/936/" target="_blank"><img src="https://imgs.xkcd.com/comics/password_strength.png" 
alt="Buy Me A Coffee" height="100%" width="80%"></a>

Traditional password policies used to recommend something like this:
- Minimum 8 characters
- 3 out of 4 complexity criteria:
    - Lowercase
    - Uppercase
    - Number
    - Symbol
- Change every 90 days

The problem with these policies are, that these will create weak passwords through the constant need to change the
password and will perhaps create passwords like this: `Spring2022`  
The password has a fixed format and is easy to break for an attacker with a [brute-force attack](https://en.wikipedia.org/wiki/Brute-force_attack) or a [dictionary attack](https://en.wikipedia.org/wiki/Dictionary_attack).

The only part, which slows a hacker down, who is trying to crack your password hash is the length of your password. In fact it can slow an attacker so much down that the ROI is negative and the attacker will eventually just give up 
cracking the password.

To get back to the picture above we can use a passphrase with random words to get a nice long password with the
ability to remember it. We can even use a space in the password to seperate the words.
Humans make and break security so educate your users about a better password policy and enforce it on the 
organizational level.

## Password guidelines for administrators :computer:
Here are some tips to get a more secure password system by password diversity:
- Maintain a high-character minimum length requirement
- Don't require complexity criteria
- Don't require periodic Password Changes
- Ban common passwords
- Educate your user
- Use multi-factor authentication when possible
- Check passwordless authenthication: `Hardware token, Keycard, etc.`


## Password guidelines for humans :busts_in_silhouette:
Here are some tips for your user in your organization:
- Use long passphrases as passwords `24+ Characters`
- Don't reuse passwords


## Source 
Check the microsoft article for more guidelines:  
https://docs.microsoft.com/en-us/microsoft-365/admin/misc/password-policy-recommendations
