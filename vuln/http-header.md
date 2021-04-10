# HTTP HEADER INJECTION
## Cara Identifikasi
  - [How to identify and exploit HTTP Host header vulnerabilities](https://portswigger.net/web-security/host-header/exploiting)
  - [Rewinding Back to the Basics — Injection Attack Series](https://medium.com/@vanessamorales.1023/rewinding-back-to-the-basics-injection-attack-series-226d35d7994e)

## User-agent
Untuk menyisipkan payload, bisa XSS atau SQL-injection.
  - [Access to staging environment via User-Agent string](https://medium.com/@yassergersy/access-to-staging-environment-via-user-agent-string-23470546577f)
  - [SQL injection through User-Agent](https://medium.com/@frostnull/sql-injection-through-user-agent-44a1150f6888)

## X-Forwarded-Host
untuk mengarahkan ke situs tertentu (attacker).
  - [Hijacking Reset Password Link in https://www.niteflirt.com/ via Host Header Poisoning (Write Up) ](https://blog.evanricafort.com/2021/02/hijacking-reset-password-link-in.html)

## X-Original-URL / X-Rewrite-Url
Untuk override sebuah request 
