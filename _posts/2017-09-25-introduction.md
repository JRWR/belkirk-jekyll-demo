---
title: Welcome to the Forestry Demo Site!
date: 2017-09-25T09:09:13.000+00:00
related_posts:
- _posts/2017-02-12-modern.md
- _posts/2017-08-01-welcome.md
sub_heading: An introduction to Forestry
tags:
- Demo
- Forestry
layout: post
banner_image: ''

---
Active Directory

· Have Interview with client and ask about:

o Default Password policy

o Ask for all subnets to scan (if not already addressed)

o Do IT Administrators or Domain Administrators use 2 accounts (one standard and one administrative) _*Note* Ask this question after scanning and reviewing users_

o Do they have EOL machines and do they segregate them from their main production network.

o Do they clean their Active Directory regularly to remove old or antiquated PCs or accounts

o Do you have any type of CNC or specialized machines

o Are users local administrators on PCs and why?

· Run RapidFire. Reference Active Directory Assessment SOP for install steps.

a. Review the report and find the following

i. PCs that haven’t logged in 30 days (filter for only active machines)

ii. Find EOL machines (compare to Lansweeper or PDQ deploy to get compressive list)

iii. Review Domain Administrators

· Check to see if domain users have non-privileged standard accounts

· Review logins to see if all users are active (within 90 days)

iv. Review User accounts

· Send over list to customer to rule out service accounts from real user accounts

· Accounts that aren’t specific to a specific user, get a list of all generic accounts.

· Users that haven’t logged in 30 days (filter for only active accounts)

· Are users local administrators on their own PC (review lansweeper)

· Run WeakPassword tool from Knowbe4

a. Break down each section for either fail or good depending on the data

i. Weak Password

ii. Password Not Required

iii. DES-only Encryption

iv. Non-unique Password

v. Password Never Expires

vi. Pre-Authentication missing

vii. Empty Passwords/Passwords not required

viii. LM Hashes

ix. Clear Text Passwords

x. AES Keys Missing

· Review GPO on Domain Controller

a. Review Default Domain Policy

i. Save as HTML report

b. Run at least 2 RSOP for a computer and user

i. Save as HTML report

c. Review RSOPs and find:

i. Password Policy

· Review password requirements.xlsx

ii. Account Lockout Policy

iii. Windows Update Policy (WSUS)

iv. Auto Lock Policy (Secure Screen Saver)

v. Any other type of security based policy as needed

_vi. *Note* Needs to be updated with further points to review for GPO policies in future assessments_

d. After reviewing save any other policy’s report to support your findings for above.

· Run Lansweeper

a. Review if users on their respective PCs are local administrators

b. Review EOL Machines from Lansweeper

i. When listing EOL systems, ensure you separate servers and workstations into their own “issue”

c. After Landsweeper is ran for several days, review logins for servers to see what admin users are logging in normally as well as users.

· Run Nessus CIS baseline against all current customers baseline

o Then use excel file to review the differences between the NIST and Customers baseline.

o Calculate the % of how out of compliance with NIST baseline.

o Inject in report.

· Ask if client has policy of restricting hours or useable hours for users to have access to log in to their systems.

o Review GPO for session terminates

o Review AD to see if user accounts have time restrictions

o Review how NTP is being issued

o Review if Warning banners are being applied in GPO

o Review if Refuse Password GPO is enabled/disabled

· Password Compliancy WITH MFA in environment –

o Still would want 14 characters

§ User training on passphrases not regular passwords

o Min Pass age – 1

o Max Pass Age – 8 or more with MFA. 14 or more without.

[https://pages.nist.gov/800-63-3/sp800-63b.html](https://pages.nist.gov/800-63-3/sp800-63b.html "https://pages.nist.gov/800-63-3/sp800-63b.html") - password regulation