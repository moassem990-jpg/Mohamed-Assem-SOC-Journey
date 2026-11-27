Phishing Analysis Fundamentals

Overview

This room introduced the fundamentals of phishing email analysis and the techniques used by SOC analysts to identify suspicious messages, investigate email headers, and handle potentially malicious links and attachments safely.

1. Email Address Structure

An email address consists of three main parts:

- Username
- "@" symbol
- Domain

Example: "hatsalesman@tryhatme.com"

The domain is "tryhatme.com".

2. How Email Works

- SMTP (Simple Mail Transfer Protocol): Used to send emails between clients and mail servers, and between mail servers.
- DNS (Domain Name System): Helps identify the receiving mail server using DNS records such as MX.
- POP3 (Post Office Protocol 3): Retrieves emails, commonly downloading them to a device.
- IMAP (Internet Message Access Protocol): Synchronizes emails across the mail server and multiple devices.

3. Email Components

- Header: Contains metadata such as sender, recipient, subject, timestamp, and message routing information.
- Body: Contains the actual message content, which may be plain text or HTML.
- Message Source: The raw email content, useful for examining headers, links, and attachments.

In Thunderbird, the message source can be viewed through "View → Message Source" or by pressing "Ctrl + U".

4. Important Email Header Fields

Header Field| Purpose
From| Displays the sender address.
To| Displays the recipient address.
Reply-To| Specifies the address used when replying.
Subject| Displays the email subject.
X-Originating-IP| May indicate the originating IP associated with the message.
Authentication-Results| Contains email authentication results, such as SPF, DKIM, and DMARC.

These fields should be examined together. No single field is sufficient to establish whether an email is legitimate.

5. Types of Email-Based Attacks

- Spam: Unsolicited bulk messages.
- Phishing: Fraudulent messages designed to trick users into revealing information or performing unsafe actions.
- Spear Phishing: Targeted phishing against a specific person or organization.
- Whaling: Phishing targeting senior executives or other high-profile individuals.
- Smishing: Phishing through SMS messages.
- Vishing: Phishing through voice calls.
- Business Email Compromise (BEC): Fraud involving the impersonation or compromise of business email identities to manipulate employees into transferring money or taking unauthorized actions.

6. Suspicious Indicators

Common phishing indicators include:

- Spoofed or misleading sender addresses.
- Domains that imitate legitimate organizations.
- Urgent or unusual requests.
- Hidden, shortened, or suspicious links.
- Unexpected attachments.
- A mismatch between the claimed organization and the actual sender domain.

Analysts should investigate the sender, domain, headers, links, attachments, and message context rather than relying on logos or display names.

7. Defanging URLs and IP Addresses

Defanging modifies indicators so they cannot be accidentally opened or clicked during analysis.

Example:

"http://suspiciousdomain.com"

Becomes:

"hxxp[://]suspiciousdomain[.]com"

This is useful when documenting and sharing indicators of compromise (IOCs).

Suspicious links and attachments should not be opened directly during investigation.

8. Practical Lab Findings

Email Sample: email1.eml

- Subject: Help protect your budget by protecting your home
- X-Originating-IP: "43.255.56.161"
- Attachment type: PDF
- Attachment filename: "zmqpalgh.pdf"
- Lab classification: Benign PDF attachment.

Email Sample: email3.eml

- Impersonated organization: Home Depot
- Sender address: "support@teckbe.com"
- X-Originating-IP: "103[.]234[.]236[.]83"
- Authentication-Results server: "atlas102.free.mail.gq1.yahoo.com"

These findings demonstrate why analysts should compare the claimed sender identity with the actual email domain and inspect the raw message source.

9. Key Takeaways

- Email headers provide valuable investigation evidence.
- Sender display names should never be trusted without verification.
- DNS, SMTP, POP3, and IMAP have different roles in email communication.
- SPF, DKIM, and DMARC results can support email authentication analysis.
- Defanging helps prevent accidental interaction with suspicious indicators.
- Attachments and links should be handled carefully during investigations.

Conclusion

This room provided practical introductory knowledge of phishing analysis, email structure, header investigation, and suspicious indicator handling. These skills are important for SOC analysts when triaging and investigating potentially malicious emails.

---

Training Platform: TryHackMe
Room: Phishing Analysis Fundamentals
Learning Track: Blue Team / SOC Analyst
Note: This report documents educational lab findings and does not represent professional incident-response experience.
