# 🔒 Vulnerability in Forgot Password System

## Description

This repository documents a critical vulnerability found in the forgot password functionality of the website [sandeepsappal.in](https://sandeepsappal.in/). The vulnerability allows for account takeover using only the victim's email ID. This security flaw is severe as it permits unauthorized access to user accounts, which could lead to sensitive data breaches.

## Steps to Reproduce

1. **Open the Website**: 
   - Navigate to [sandeepsappal.in](https://sandeepsappal.in/).
   
2. **Initiate Forgot Password**: 
   - Use the "Forgot Password" functionality.
   - Enter the victim's email ID.

3. **Intercept the Request**: 
   - Use Burp Suite (Proxy intercept) to intercept the request.
   - Observe that the password reset link is exposed during interception.

4. **Copy and Paste the Link**: 
   - Copy the reset link from the intercepted request.
   - Paste the link into another browser window or tab.

5. **Change the Password**: 
   - Follow the link and change the password successfully.

6. **Login to the Victim's Account**: 
   - Use the new password to log in to the victim's account.

## Example Exploitation

The vulnerability was demonstrated with the consent of a friend, Naveen Mittal. The following steps were taken:

1. Initiated a password reset for Naveen Mittal's account.
2. Intercepted the password reset link using Burp Suite.
3. Changed the password successfully.
4. Logged into Naveen Mittal's account using the new password.

## Impact

This vulnerability allows an attacker to take over any user's account by simply knowing their email ID. This can lead to unauthorized access to sensitive information, data theft, and potential misuse of account privileges.

## Mitigation

To address this vulnerability, the following steps should be taken:

1. **Encrypt Password Reset Links**: Ensure that password reset links are encrypted and valid only for a short duration.
2. **Verify User Identity**: Implement additional verification steps, such as security questions or two-factor authentication, before allowing a password reset.
3. **Log and Monitor**: Regularly monitor logs for unusual password reset activities and alert users of suspicious behavior.
4. **Secure Communication**: Use secure communication protocols to protect the transmission of sensitive information.

## Thank You! 😊

Thank you for taking the time to read through this documentation. Let's work together to make the web a safer place! Happy hacking! 🚀🔐

---

**Disclaimer**: This document is for educational purposes only. Exploiting security vulnerabilities without proper authorization is illegal and unethical.

## License

This project is licensed under the MIT License. See the LICENSE file for details.
