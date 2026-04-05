# Email Header Analyzer

I built this tool because I noticed that most people — even tech-savvy ones — 
have no idea how to read raw email headers. And that's exactly what attackers 
exploit. This is a simple browser-based tool that does the heavy lifting for you.

No installations. No setup. Just open the HTML file and paste your headers.

---

## Why I built this

Email spoofing is behind most of the phishing attacks we hear about. The scary 
part is that a spoofed email can look completely legitimate on the surface — same 
logo, same sender name — but the headers tell a completely different story.

I wanted to build something that makes those hidden red flags visible, even to 
someone who has never heard of SPF or DKIM before.

---

## What it checks

- SPF — is the sending server actually allowed to send from this domain?
- DKIM — was the email modified after it was sent?
- Reply-To mismatch — will your reply go somewhere completely different?
- Return-Path — does the bounce address match the sender?
- Domain reputation — is the sender domain suspicious?
- Originating IP — where did this email actually come from?
- Routing hops — did this email bounce through an unusual number of servers?

Everything gets rolled into a threat score out of 100.

---

## How to use it

1. Download the HTML file
2. Open it in your browser
3. Paste your raw email headers
4. Hit Analyze

If you want to test it without a real email, just click the 
"Load Sample Suspicious Email" button — it loads a fake phishing header 
so you can see how the tool flags it.

---

## How to get raw headers from your email

- Gmail → open the email → three dots → Show original
- Outlook → open the email → File → Properties → Internet headers
- Yahoo → open the email → three dots → View raw message

---

## Tech

Just plain HTML, CSS and JavaScript. No frameworks, no libraries, no backend. 
Runs entirely in the browser and works offline.

---

Built by Svara Srivastava — B.Tech CSE (Cybersecurity), AKTU
