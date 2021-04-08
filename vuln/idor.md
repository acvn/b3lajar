# INSECURE DIRECT OBJECT REFERENCE

## Tools
- Browser
  - Use the browser’s secret tab to quickly practically test IDOR vulnerabilities. So, when you use the regular tab as a normal user, you can use the secret tab as an attacker. This will ensure that you don’t logout.
- Burpsuite
  - Use burpsuite's HTTP history tab for checking all of requests.
  - Use burpsuite's scope feature for fast testing.
  - Use burpsuite’s compare tool.
  - AuthMAtrix
## Tips and trics
  - Focus on 1 feature (Pak Yokokho)
  - [How-To: Find IDOR (Insecure Direct Object Reference) Vulnerabilities for large bounty rewards](https://www.bugcrowd.com/blog/how-to-find-idor-insecure-direct-object-reference-vulnerabilities-for-large-bounty-rewards/)
  - [Everything You Need to Know About IDOR (Insecure Direct Object References)](https://aysebilge.com/2020/04/17/everything-you-need-to-know-about-idor)
    - Log in to the same application with 2 different user roles. If you’d like to you can use different to perform this action or you can log in with user-1 to regular window and with user-2 to incognito window.
    - List all endpoints in the application.
    - Try perform on endpoints for cross user roles. You can use AuthMatrix in BurpSuite.
    - If you can read, update, create or delete an endpoint you’re not authorized then there is an IDOR.


## Case
- [IDOR via Websockets allow me to takeover any users account](https://mokhansec.medium.com/idor-via-websockets-allow-me-to-takeover-any-users-account-23460dacdeab)
  - Always play with login, signup, and change info functionality. There is always something for you 

