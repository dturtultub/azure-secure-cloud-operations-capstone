{\rtf1\ansi\ansicpg1252\cocoartf2868
\cocoatextscaling0\cocoaplatform0{\fonttbl\f0\fswiss\fcharset0 Helvetica;}
{\colortbl;\red255\green255\blue255;}
{\*\expandedcolortbl;;}
\margl1440\margr1440\vieww11520\viewh8400\viewkind0
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\partightenfactor0

\f0\fs24 \cf0 # Conditional Access Admin MFA + Device Control\
\
## Goal\
\
Build a Microsoft Entra Conditional Access policy that protects privileged administrator access.\
\
The policy requires administrators to use MFA and a trusted device when signing in from untrusted locations.\
\
## Why this matters\
\
This lab demonstrates identity security, privileged access protection, MFA enforcement, device-based access control, and sign-in log validation.\
\
## Source questions\
\
- B001-Q002\
- B001-Q003\
- B001-Q004\
\
## AZ-104 concepts\
\
- Microsoft Entra ID\
- Conditional Access\
- MFA\
- Grant controls\
- Session controls\
- Trusted locations\
- Sign-in logs\
- Privileged administrator protection\
\
## Resume value\
\
High.\
\
This is stronger than a basic VM lab because identity security and administrator access control are common real-world cloud admin responsibilities.\
\
## Screenshots to capture\
\
1. 01-policy-overview.png\
2. 02-users-global-admins-targeted.png\
3. 03-conditions-locations.png\
4. 04-grant-controls-mfa-device-required.png\
5. 05-report-only-mode.png\
6. 06-sign-in-logs-validation.png\
\
## Real-world explanation\
\
A cloud administrator should not allow privileged users to sign in from risky or untrusted locations without extra controls.\
\
Conditional Access allows an organization to require stronger authentication and trusted device conditions before allowing access.\
\
## Resume bullet\
\
Built a Microsoft Entra Conditional Access policy targeting privileged administrators, requiring MFA and trusted device controls from untrusted locations, with validation through sign-in logs.\
\
## Interview explanation\
\
Per-user MFA changes a user's MFA state, but it does not fully express conditions like location, device trust, and admin-role targeting.\
\
For this requirement, the correct solution is a Conditional Access policy using grant controls because the organization wants access granted only when MFA and device requirements are satisfied.\
}