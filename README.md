# Philosophy of [hacksecu.re](https://hacksecu.re)
## What is this?
At its most basic,[hacksecu.re](https://hacksecu.re) is a web app designed to give hackers feedback on the security and privacy of any hackathon website. 
## What do you mean by security?
We send and receive a lot of valuable information on the internet. Ensuring that it can't be interpreted by anybody who has access to your data in-transit is the purpose of SSL [^1]. Hackathon websites often collect a lot of sensitive data: your name, email address, school, career interest & passwords [^2]. Ensuring that this content is encrypted from the user to the server is the purpose of SSL.

To be clear, when it comes to security, [hacksecu.re](https://hacksecu.re) is only concerned with SSL. It's very possible[^3] that many hackathons have insecure servers and databases. However, there is no uniform way to scan and determine this. At a minimum, the set of people who can intercept a connection over a local network is much larger than the set of people with the know-how to break into a server or find a database with a bad password. 

### Aside: What about websites that don't collect personal information?
There are plenty of hackathons that don't collect information on their site and instead pass off the responsibility to Google Forms or Typeform. That's a good thing! Basically all companies will have a more secure platform than something that a hackathon builds on its own simply because companies can employ a full-time dev team or even a full-time security team. However, delivering a website over plaintext still has risks. First of all, it can tell anyone with access to your connection that you're interesting in hacking and CS generall. In the US, that now includes your ISP. Access to your web history like this is incredibly powerful. It also allows a man in the middle (MITM) attack. Attacks like this involve an attacker interecept your website in transit and changing it. For example, they could change https://your-application-form.com to https://evil-application-form-scary-scary.com. SSL is the **only** way to trust that the content you're receiving is the same as what the server sent. 

## What do you mean by privacy?
We think privacy is important and that embedded trackers in websites suck. That said, having a tracker in your website isn't necessarily a bad thing in the same way delivering a website over an unencrypted connection is. For example, Google Analytics gives incredibly powerful information to webadmins in exchange for giving Google that same information (albeit in a more anonmyized form). Regardless, we feel that users should be able to know about these trackers and judge for themselves if they're OK with what a website is serving. 

## So why does this site exist?
This site, modeled off of https://securethe.news/, aims to provide an easy-to-consult list of collegiate hackathons across the world and the security of their website. We hope that, over time, getting a 100 will be a goal of hackathons. We also hope that this site will lead to increased awareness and activism regarding site security in the hackathon community. 


## Licensing
All code under this project will be licensed under the MIT License. Any content in the repo is under the CC BY-SA 4.0 license or what is in the `LICENSE.md` file. If the `LICENSE.md` file differs from what is stated in the Markdown file, then default to the `LICENSE.md` file.

[^1]: Today, browsers use a more modern encryption schema called TLS so the term "SSL" has been relegated to generally referring to any form of encrypting data in-transit on the web. 

[^2]: Statistically, these passwords are reused by most people for accounts much more important than a hacker application.

[^3]: Realistically, probable.