# CSRF

Cross Site Request Forgery / Onelink Attack adalah serangan yang memaksa pengguna agar backend mengeksekusi perintah yang tidak seharusnya dizinkan, menipu website dari request user yang terpercaya dan mengirim Request palsu dari authenticate user.

## CSRF Token as CSRF Protection
- CSRF token should be generated on the server-side
- CSRF token should not be transmitted using cookies
- CSRF token should be unique per session, secret, and unpredictable
- CSRF token should no be leaked in the server logs or in the URL

## How to find them ?
```
The easiest way to check whether an application is vulnerable is to see if each link and form contains an unpredictable token for each user. Without such an unpredictable token, attackers can forge malicious requests. Focus on the links and forms that invoke state-changing functions, since those are the most important CSRF targets.
```
- Gunakan burpsuite untuk melihat dan merubah csrf token yang terkandung pada HTTP request
- [Mengganti content-type non-form  (i.e. `application/json, application/x-url-encoded`, etc.) menjadi `form-multipart`](https://medium.com/bugbountywriteup/refocusing-in-bug-hunting-bonus-an-interestingly-simple-to-test-csrf-bypass-8595b3312147)
- Gonta-ganti method, POST ke GET, atau sebaliknya
- Mengganti nilai csrf token dengan length yang sama
- Spoof Anti-CSRF Token by Changing a few bits
- Using Same Anti-CSRF Token
- Guessable Anti-CSRF Token
- Stealing Token with other attacks such as XSS
- Contoh Payload,
  ```
  <form method="$method" action="$url">
    <input type="hidden" name="$param1name" value="$param1value">
  </form>
  <script>
    document.forms[0].submit();
  </script>
  ```
## Prevention
- Samesite Cookie (bisa dibypass dengan modifikasi GET)
![image](https://user-images.githubusercontent.com/52058660/120603439-3cca2d80-c476-11eb-8de1-2d803a2a4c45.png)

## Resource
- [SKF - CSRF](https://owasp-skf.gitbook.io/asvs-write-ups/kbid-5-csrf)
- [OWASP - Cross Site Request Forgery (CSRF)](https://owasp.org/www-community/attacks/csrf)
- [OWASP - Reviewing Code for Cross-Site Request Forgery Issues
Overview](https://owasp.org/www-project-code-review-guide/reviewing-code-for-csrf-issues)
- [OWASP Web Security Testing Guide - Testing for Cross Site Request Forgery](https://github.com/OWASP/wstg/blob/master/document/4-Web_Application_Security_Testing/06-Session_Management_Testing/05-Testing_for_Cross_Site_Request_Forgery.md)
- [OWASP Cheat Sheet Series - Cross-Site Request Forgery Prevention Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Cross-Site_Request_Forgery_Prevention_Cheat_Sheet.html)

## Write-up
- [CSRF at Kaskus.co.id](https://medium.com/@daffailhamr/csrf-at-kaskus-co-id-f8e31864807f)

## Lab
- [Portswigger Academy - Cross-site request forgery (CSRF)](https://portswigger.net/web-security/csrf)
- [OWASP Juice Shop - Broken Access Control](https://owasp.org/www-project-juice-shop/)
