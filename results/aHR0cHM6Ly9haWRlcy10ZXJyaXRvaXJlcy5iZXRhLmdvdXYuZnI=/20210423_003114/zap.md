
# ZAP Scanning Report

Generated on Fri, 23 Apr 2021 00:22:52


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 3 |
| Low | 8 |
| Informational | 6 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Reverse Tabnabbing | Medium | 12 | 
| X-Frame-Options Header Not Set | Medium | 11 | 
| Absence of Anti-CSRF Tokens | Low | 12 | 
| Cookie No HttpOnly Flag | Low | 12 | 
| Dangerous JS Functions | Low | 3 | 
| Feature Policy Header Not Set | Low | 11 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 11 | 
| Private IP Disclosure | Low | 4 | 
| Strict-Transport-Security Header Not Set | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 12 | 
| Base64 Disclosure | Informational | 11 | 
| Information Disclosure - Suspicious Comments | Informational | 3 | 
| Modern Web Application | Informational | 12 | 
| Non-Storable Content | Informational | 2 | 
| Storable and Cacheable Content | Informational | 9 | 
| Timestamp Disclosure - Unix | Informational | 10 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/connexion/](https://aides-territoires.beta.gouv.fr/comptes/connexion/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/porteurs-aides/](https://aides-territoires.beta.gouv.fr/porteurs-aides/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/inscription/](https://aides-territoires.beta.gouv.fr/comptes/inscription/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/robots.txt/](https://aides-territoires.beta.gouv.fr/robots.txt/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/data/](https://aides-territoires.beta.gouv.fr/data/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/](https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/recherche/formulaire/audience/](https://aides-territoires.beta.gouv.fr/recherche/formulaire/audience/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/](https://aides-territoires.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/](https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/contact/](https://aides-territoires.beta.gouv.fr/contact/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr](https://aides-territoires.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to set the Content-Security-Policy header, to achieve optimal browser support: "Content-Security-Policy" for Chrome 25+, Firefox 23+ and Safari 7+, "X-Content-Security-Policy" for Firefox 4.0+ and Internet Explorer 10+, and "X-WebKit-CSP" for Chrome 14+ and Safari 6+.</p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/Security/CSP/Introducing_Content_Security_Policy
* https://cheatsheetseries.owasp.org/cheatsheets/Content_Security_Policy_Cheat_Sheet.html
* http://www.w3.org/TR/CSP/
* http://w3c.github.io/webappsec/specs/content-security-policy/csp-specification.dev.html
* http://www.html5rocks.com/en/tutorials/security/content-security-policy/
* http://caniuse.com/#feat=contentsecuritypolicy
* http://content-security-policy.com/

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Reverse Tabnabbing
##### Medium (Medium)
  
  
  
  
#### Description
<p>At least one link on this page is vulnerable to Reverse tabnabbing as it uses a target attribute without using both of the "noopener" and "noreferrer" keywords in the "rel" attribute, which allows the target page to take control of this page.</p>
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/](https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://twitter.com/aidesterr" title="Retrouvez Aides territoires sur Twitter" target="_blank" rel="noopener"><img src="/static/img/logo_twitter.svg" alt="logo twitter"></a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/inscription/](https://aides-territoires.beta.gouv.fr/comptes/inscription/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://twitter.com/aidesterr" title="Retrouvez Aides territoires sur Twitter" target="_blank" rel="noopener"><img src="/static/img/logo_twitter.svg" alt="logo twitter"></a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/](https://aides-territoires.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://www.eau-grandsudouest.fr/" target="_blank">
                    
                        
                        <img src="https://aides-territoires-prod.s3.fr-par.scw.cloud/aides-territoires-prod/backers/agence-de-leau-adour-garonne_logo.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&amp;X-Amz-Credential=SCWJ1T6VQNR6Z83FSYEB%2F20210423%2Ffr-par%2Fs3%2Faws4_request&amp;X-Amz-Date=20210423T002041Z&amp;X-Amz-Expires=3600&amp;X-Amz-SignedHeaders=host&amp;X-Amz-Signature=9bb46ed51c45becae60e6fda75a3c22705d98c32bd940fd706ef0db6feec1686" alt="Logo : Agence de l&#x27;eau Adour-Garonne ">
                        
                    </a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/](https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://radioterritoria.fr/broadcast/3105-Aides-Territoires-la-plateforme-qui-permet-aux-territoires-de-trouver-des-aides-pour-financer-et-accompagner-leurs-projets-locaux" rel="noopener" target="_blank">
   Radio Territoria
  </a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/contact/](https://aides-territoires.beta.gouv.fr/contact/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://twitter.com/aidesterr" title="Retrouvez Aides territoires sur Twitter" target="_blank" rel="noopener"><img src="/static/img/logo_twitter.svg" alt="logo twitter"></a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/recherche/formulaire/audience/](https://aides-territoires.beta.gouv.fr/recherche/formulaire/audience/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://twitter.com/aidesterr" title="Retrouvez Aides territoires sur Twitter" target="_blank" rel="noopener"><img src="/static/img/logo_twitter.svg" alt="logo twitter"></a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/connexion/](https://aides-territoires.beta.gouv.fr/comptes/connexion/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://twitter.com/aidesterr" title="Retrouvez Aides territoires sur Twitter" target="_blank" rel="noopener"><img src="/static/img/logo_twitter.svg" alt="logo twitter"></a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr](https://aides-territoires.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://www.agencebio.org/" target="_blank">
                    
                        
                        <img src="https://aides-territoires-prod.s3.fr-par.scw.cloud/aides-territoires-prod/backers/agence-bio_logo.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&amp;X-Amz-Credential=SCWJ1T6VQNR6Z83FSYEB%2F20210423%2Ffr-par%2Fs3%2Faws4_request&amp;X-Amz-Date=20210423T002044Z&amp;X-Amz-Expires=3600&amp;X-Amz-SignedHeaders=host&amp;X-Amz-Signature=67a6ec39a069439b57703d46c6b9d80ceb577f8495cb88ab95018d06151d3147" alt="Logo : Agence BIO ">
                        
                    </a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/](https://aides-territoires.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://www.ademe.fr/" target="_blank">
                    
                        
                        <img src="https://aides-territoires-prod.s3.fr-par.scw.cloud/aides-territoires-prod/backers/ademe_logo.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&amp;X-Amz-Credential=SCWJ1T6VQNR6Z83FSYEB%2F20210423%2Ffr-par%2Fs3%2Faws4_request&amp;X-Amz-Date=20210423T002045Z&amp;X-Amz-Expires=3600&amp;X-Amz-SignedHeaders=host&amp;X-Amz-Signature=b82b97a97465554c29800d0530d7e1c55323aee9c33f10e7e67d4b486d983c2a" alt="Logo : ADEME ">
                        
                    </a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/robots.txt/](https://aides-territoires.beta.gouv.fr/robots.txt/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://twitter.com/aidesterr" title="Retrouvez Aides territoires sur Twitter" target="_blank" rel="noopener"><img src="/static/img/logo_twitter.svg" alt="logo twitter"></a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/porteurs-aides/](https://aides-territoires.beta.gouv.fr/porteurs-aides/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://twitter.com/aidesterr" title="Retrouvez Aides territoires sur Twitter" target="_blank" rel="noopener"><img src="/static/img/logo_twitter.svg" alt="logo twitter"></a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/data/](https://aides-territoires.beta.gouv.fr/data/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://twitter.com/aidesterr" title="Retrouvez Aides territoires sur Twitter" target="_blank" rel="noopener"><img src="/static/img/logo_twitter.svg" alt="logo twitter"></a>`
  
  
  
  
Instances: 12
  
### Solution
<p>Do not use a target attribute, or if you have to then also add the attribute: rel="noopener noreferrer".</p>
  
### Reference
* https://owasp.org/www-community/attacks/Reverse_Tabnabbing
* https://dev.to/ben/the-targetblank-vulnerability-by-example
* https://mathiasbynens.github.io/rel-noopener/
* https://medium.com/@jitbit/target-blank-the-most-underestimated-vulnerability-ever-96e328301f4c

  
#### Source ID : 3

  
  
  
  
### X-Frame-Options Header Not Set
##### Medium (Medium)
  
  
  
  
#### Description
<p>X-Frame-Options header is not included in the HTTP response to protect against 'ClickJacking' attacks.</p>
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/mentions-l%C3%A9gales/](https://aides-territoires.beta.gouv.fr/mentions-l%C3%A9gales/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/recherche/formulaire/audience/](https://aides-territoires.beta.gouv.fr/recherche/formulaire/audience/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/data/](https://aides-territoires.beta.gouv.fr/data/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/porteurs-aides/](https://aides-territoires.beta.gouv.fr/porteurs-aides/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/inscription/](https://aides-territoires.beta.gouv.fr/comptes/inscription/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/](https://aides-territoires.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/contact/](https://aides-territoires.beta.gouv.fr/contact/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/](https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr](https://aides-territoires.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/connexion/](https://aides-territoires.beta.gouv.fr/comptes/connexion/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/](https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
Instances: 11
  
### Solution
<p>Most modern Web browsers support the X-Frame-Options HTTP header. Ensure it's set on all web pages returned by your site (if you expect the page to be framed only by pages on your server (e.g. it's part of a FRAMESET) then you'll want to use SAMEORIGIN, otherwise if you never expect the page to be framed, you should use DENY. Alternatively consider implementing Content Security Policy's "frame-ancestors" directive. </p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Absence of Anti-CSRF Tokens
##### Low (Medium)
  
  
  
  
#### Description
<p>No Anti-CSRF tokens were found in a HTML submission form.</p><p>A cross-site request forgery is an attack that involves forcing a victim to send an HTTP request to a target destination without their knowledge or intent in order to perform an action as the victim. The underlying cause is application functionality using predictable URL/form actions in a repeatable way. The nature of the attack is that CSRF exploits the trust that a web site has for a user. By contrast, cross-site scripting (XSS) exploits the trust that a user has for a web site. Like XSS, CSRF attacks are not necessarily cross-site, but they can be. Cross-site request forgery is also known as CSRF, XSRF, one-click attack, session riding, confused deputy, and sea surf.</p><p></p><p>CSRF attacks are effective in a number of situations, including:</p><p>    * The victim has an active session on the target site.</p><p>    * The victim is authenticated via HTTP auth on the target site.</p><p>    * The victim is on the same local network as the target site.</p><p></p><p>CSRF has primarily been used to perform an action against a target site using the victim's privileges, but recent techniques have been discovered to disclose information by gaining access to the response. The risk of information disclosure is dramatically increased when the target site is vulnerable to XSS, because XSS can be used as a platform for CSRF, allowing the attack to operate within the bounds of the same-origin policy.</p>
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/2e27-moderniser-les-librairies-aide-a-la-modernisa/](https://aides-territoires.beta.gouv.fr/aides/2e27-moderniser-les-librairies-aide-a-la-modernisa/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="copy-to-clipboard-form">`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/8961-copie-10h22-renforcer-le-programme-dhumanisat/](https://aides-territoires.beta.gouv.fr/aides/8961-copie-10h22-renforcer-le-programme-dhumanisat/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="copy-to-clipboard-form">`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/63c2-recenser-et-evaluer-les-ouvrages-dart-des-pet/](https://aides-territoires.beta.gouv.fr/aides/63c2-recenser-et-evaluer-les-ouvrages-dart-des-pet/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="copy-to-clipboard-form">`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/e285-norrr-appel-a-projet-pour-financer-des-equipe/](https://aides-territoires.beta.gouv.fr/aides/e285-norrr-appel-a-projet-pour-financer-des-equipe/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="copy-to-clipboard-form">`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/recherche/formulaire/audience/](https://aides-territoires.beta.gouv.fr/recherche/formulaire/audience/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="audience" action="/recherche/formulaire/territoire/" method="GET">`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/9d50-copie-12h10-etudier-la-faisabilite-dun-projet/](https://aides-territoires.beta.gouv.fr/aides/9d50-copie-12h10-etudier-la-faisabilite-dun-projet/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="copy-to-clipboard-form">`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/1185-favoriser-et-developper-les-iniatiatives-perm/](https://aides-territoires.beta.gouv.fr/aides/1185-favoriser-et-developper-les-iniatiatives-perm/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="copy-to-clipboard-form">`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/8740-reemploiet-reemploi-reutilisation-aide-aux-et/](https://aides-territoires.beta.gouv.fr/aides/8740-reemploiet-reemploi-reutilisation-aide-aux-et/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="copy-to-clipboard-form">`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/2410-eitcentre-accompagnement-de-demarches-decolog/](https://aides-territoires.beta.gouv.fr/aides/2410-eitcentre-accompagnement-de-demarches-decolog/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="copy-to-clipboard-form">`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/c131-parcours-de-cybersecurite/](https://aides-territoires.beta.gouv.fr/aides/c131-parcours-de-cybersecurite/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="copy-to-clipboard-form">`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/5442-deployer-les-micro-folies-en-ile-de-france/](https://aides-territoires.beta.gouv.fr/aides/5442-deployer-les-micro-folies-en-ile-de-france/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="copy-to-clipboard-form">`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/c216-rrr-reemploi-reparation-reutilisation-/](https://aides-territoires.beta.gouv.fr/aides/c216-rrr-reemploi-reparation-reutilisation-/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="copy-to-clipboard-form">`
  
  
  
  
Instances: 12
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 1: "currentUrl" ].</p>
  
### Reference
* http://projects.webappsec.org/Cross-Site-Request-Forgery
* http://cwe.mitre.org/data/definitions/352.html

  
#### CWE Id : 352
  
#### WASC Id : 9
  
#### Source ID : 3

  
  
  
  
### Cookie No HttpOnly Flag
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the HttpOnly flag, which means that the cookie can be accessed by JavaScript. If a malicious script can be run on this page then the cookie will be accessible and can be transmitted to another site. If this is a session cookie then session hijacking may be possible.</p>
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/e285-norrr-appel-a-projet-pour-financer-des-equipe/](https://aides-territoires.beta.gouv.fr/aides/e285-norrr-appel-a-projet-pour-financer-des-equipe/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/9d50-copie-12h10-etudier-la-faisabilite-dun-projet/](https://aides-territoires.beta.gouv.fr/aides/9d50-copie-12h10-etudier-la-faisabilite-dun-projet/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/2e27-moderniser-les-librairies-aide-a-la-modernisa/](https://aides-territoires.beta.gouv.fr/aides/2e27-moderniser-les-librairies-aide-a-la-modernisa/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/8961-copie-10h22-renforcer-le-programme-dhumanisat/](https://aides-territoires.beta.gouv.fr/aides/8961-copie-10h22-renforcer-le-programme-dhumanisat/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/5442-deployer-les-micro-folies-en-ile-de-france/](https://aides-territoires.beta.gouv.fr/aides/5442-deployer-les-micro-folies-en-ile-de-france/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/connexion/](https://aides-territoires.beta.gouv.fr/comptes/connexion/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/inscription/](https://aides-territoires.beta.gouv.fr/comptes/inscription/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/c216-rrr-reemploi-reparation-reutilisation-/](https://aides-territoires.beta.gouv.fr/aides/c216-rrr-reemploi-reparation-reutilisation-/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/contact/](https://aides-territoires.beta.gouv.fr/contact/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/c131-parcours-de-cybersecurite/](https://aides-territoires.beta.gouv.fr/aides/c131-parcours-de-cybersecurite/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/8740-reemploiet-reemploi-reutilisation-aide-aux-et/](https://aides-territoires.beta.gouv.fr/aides/8740-reemploiet-reemploi-reutilisation-aide-aux-et/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/1185-favoriser-et-developper-les-iniatiatives-perm/](https://aides-territoires.beta.gouv.fr/aides/1185-favoriser-et-developper-les-iniatiatives-perm/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
Instances: 12
  
### Solution
<p>Ensure that the HttpOnly flag is set for all cookies.</p>
  
### Reference
* https://owasp.org/www-community/HttpOnly

  
#### CWE Id : 16
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Dangerous JS Functions
##### Low (Low)
  
  
  
  
#### Description
<p>A dangerous JS function seems to be in use that would leave the site vulnerable.</p>
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/63c2-recenser-et-evaluer-les-ouvrages-dart-des-pet/](https://aides-territoires.beta.gouv.fr/aides/63c2-recenser-et-evaluer-les-ouvrages-dart-des-pet/)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/CACHE/js/output.8a6e3aa6c87c.js](https://aides-territoires.beta.gouv.fr/static/CACHE/js/output.8a6e3aa6c87c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/d34e-realiser-sa-demarche-devaluation-locale-actio/](https://aides-territoires.beta.gouv.fr/aides/d34e-realiser-sa-demarche-devaluation-locale-actio/)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
Instances: 3
  
### Solution
<p>See the references for security advice on the use of these functions.</p>
  
### Reference
* https://angular.io/guide/security

  
#### CWE Id : 749
  
#### Source ID : 3

  
  
  
  
### Feature Policy Header Not Set
##### Low (Medium)
  
  
  
  
#### Description
<p>Feature Policy Header is an added layer of security that helps to restrict from unauthorized access or usage of browser/client features by web resources. This policy ensures the user privacy by limiting or specifying the features of the browsers can be used by the web resources. Feature Policy provides a set of standard HTTP headers that allow website owners to limit which features of browsers can be used by the page such as camera, microphone, location, full screen etc.</p>
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/](https://aides-territoires.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/robots.txt/](https://aides-territoires.beta.gouv.fr/robots.txt/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/](https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/porteurs-aides/](https://aides-territoires.beta.gouv.fr/porteurs-aides/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/data/](https://aides-territoires.beta.gouv.fr/data/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/](https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/inscription/](https://aides-territoires.beta.gouv.fr/comptes/inscription/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/contact/](https://aides-territoires.beta.gouv.fr/contact/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/recherche/formulaire/audience/](https://aides-territoires.beta.gouv.fr/recherche/formulaire/audience/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr](https://aides-territoires.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/connexion/](https://aides-territoires.beta.gouv.fr/comptes/connexion/)
  
  
  * Method: `GET`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to set the Feature-Policy header.</p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Feature-Policy
* https://developers.google.com/web/updates/2018/06/feature-policy
* https://scotthelme.co.uk/a-new-security-header-feature-policy/
* https://w3c.github.io/webappsec-feature-policy/
* https://www.smashingmagazine.com/2018/12/feature-policy/

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Incomplete or No Cache-control and Pragma HTTP Header Set
##### Low (Medium)
  
  
  
  
#### Description
<p>The cache-control and pragma HTTP header have not been set properly or are missing allowing the browser and proxies to cache content.</p>
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/sitemap.xml](https://aides-territoires.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/data/](https://aides-territoires.beta.gouv.fr/data/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/recherche/formulaire/audience/](https://aides-territoires.beta.gouv.fr/recherche/formulaire/audience/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/contact/](https://aides-territoires.beta.gouv.fr/contact/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/](https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/inscription/](https://aides-territoires.beta.gouv.fr/comptes/inscription/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/](https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/mentions-l%C3%A9gales/](https://aides-territoires.beta.gouv.fr/mentions-l%C3%A9gales/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr](https://aides-territoires.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/porteurs-aides/](https://aides-territoires.beta.gouv.fr/porteurs-aides/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/](https://aides-territoires.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
Instances: 11
  
### Solution
<p>Whenever possible ensure the cache-control HTTP header is set with no-cache, no-store, must-revalidate; and that the pragma HTTP header is set with no-cache.</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching

  
#### CWE Id : 525
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Private IP Disclosure
##### Low (Medium)
  
  
  
  
#### Description
<p>A private IP (such as 10.x.x.x, 172.x.x.x, 192.168.x.x) or an Amazon EC2 private hostname (for example, ip-10-0-56-78) has been found in the HTTP response body. This information might be helpful for further attacks targeting internal systems.</p>
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/e52f-accompagner-les-territoires-a-la-creation-dun/](https://aides-territoires.beta.gouv.fr/aides/e52f-accompagner-les-territoires-a-la-creation-dun/)
  
  
  * Method: `GET`
  
  
  * Evidence: `10.33.93.11`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/e6f9-mettre-en-place-une-offre-de-mobilite-pour-le/](https://aides-territoires.beta.gouv.fr/aides/e6f9-mettre-en-place-une-offre-de-mobilite-pour-le/)
  
  
  * Method: `GET`
  
  
  * Evidence: `10.33.93.11`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/8745-former-des-conseillers-mobilite/](https://aides-territoires.beta.gouv.fr/aides/8745-former-des-conseillers-mobilite/)
  
  
  * Method: `GET`
  
  
  * Evidence: `10.33.93.11`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/65c1-developper-une-ecode-de-conduite-a-statut-ass/](https://aides-territoires.beta.gouv.fr/aides/65c1-developper-une-ecode-de-conduite-a-statut-ass/)
  
  
  * Method: `GET`
  
  
  * Evidence: `10.33.93.11`
  
  
  
  
Instances: 4
  
### Solution
<p>Remove the private IP address from the HTTP response body.  For comments, use JSP/ASP/PHP comment instead of HTML/JavaScript comment which can be seen by client browsers.</p>
  
### Other information
<p>10.33.93.11</p><p></p>
  
### Reference
* https://tools.ietf.org/html/rfc1918

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Strict-Transport-Security Header Not Set
##### Low (High)
  
  
  
  
#### Description
<p>HTTP Strict Transport Security (HSTS) is a web security policy mechanism whereby a web server declares that complying user agents (such as a web browser) are to interact with it using only secure HTTPS connections (i.e. HTTP layered over TLS/SSL). HSTS is an IETF standards track protocol and is specified in RFC 6797.</p>
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/sitemap.xml](https://aides-territoires.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/recherche/formulaire/audience/](https://aides-territoires.beta.gouv.fr/recherche/formulaire/audience/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/robots.txt/](https://aides-territoires.beta.gouv.fr/robots.txt/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/data/](https://aides-territoires.beta.gouv.fr/data/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/](https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/](https://aides-territoires.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/porteurs-aides/](https://aides-territoires.beta.gouv.fr/porteurs-aides/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/inscription/](https://aides-territoires.beta.gouv.fr/comptes/inscription/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/connexion/](https://aides-territoires.beta.gouv.fr/comptes/connexion/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr](https://aides-territoires.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/](https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/)
  
  
  * Method: `GET`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to enforce Strict-Transport-Security.</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Strict_Transport_Security_Cheat_Sheet.html
* https://owasp.org/www-community/Security_Headers
* http://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security
* http://caniuse.com/stricttransportsecurity
* http://tools.ietf.org/html/rfc6797

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### X-Content-Type-Options Header Missing
##### Low (Medium)
  
  
  
  
#### Description
<p>The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.</p>
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/img/logo_AT_courbes.svg](https://aides-territoires.beta.gouv.fr/static/img/logo_AT_courbes.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/favicons/favicon.svg](https://aides-territoires.beta.gouv.fr/static/favicons/favicon.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/img/logo_RP.svg](https://aides-territoires.beta.gouv.fr/static/img/logo_RP.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/favicons/favicon.ico](https://aides-territoires.beta.gouv.fr/static/favicons/favicon.ico)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/CACHE/js/output.8a6e3aa6c87c.js](https://aides-territoires.beta.gouv.fr/static/CACHE/js/output.8a6e3aa6c87c.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/favicons/favicon.png](https://aides-territoires.beta.gouv.fr/static/favicons/favicon.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/CACHE/js/output.3367a7a8b0c1.js](https://aides-territoires.beta.gouv.fr/static/CACHE/js/output.3367a7a8b0c1.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/img/logo_AT_titre.svg](https://aides-territoires.beta.gouv.fr/static/img/logo_AT_titre.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/favicons/favicon-32x32.png](https://aides-territoires.beta.gouv.fr/static/favicons/favicon-32x32.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/CACHE/css/output.b74d336c2ebc.css](https://aides-territoires.beta.gouv.fr/static/CACHE/css/output.b74d336c2ebc.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/img/marianne.svg](https://aides-territoires.beta.gouv.fr/static/img/marianne.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/js/shared_config.js](https://aides-territoires.beta.gouv.fr/static/js/shared_config.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
Instances: 12
  
### Solution
<p>Ensure that the application/web server sets the Content-Type header appropriately, and that it sets the X-Content-Type-Options header to 'nosniff' for all web pages.</p><p>If possible, ensure that the end user uses a standards-compliant and modern web browser that does not perform MIME-sniffing at all, or that can be directed by the web application/web server to not perform MIME-sniffing.</p>
  
### Other information
<p>This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.</p><p>At "High" threshold this scan rule will not alert on client or server error responses.</p>
  
### Reference
* http://msdn.microsoft.com/en-us/library/ie/gg622941%28v=vs.85%29.aspx
* https://owasp.org/www-community/Security_Headers

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/](https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/broadcast/11984-Aides-Territoires-qu-est-ce-que-c-est`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/robots.txt/](https://aides-territoires.beta.gouv.fr/robots.txt/)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/serve/MUIEANv2FVIgFOCSUcH4G40Mz7-gNNDCYBU1BnExyPfqcBds83BFiunc-uCZL1sFeaqWrXMAu2qntWXa4I6Y9qxHK1t4nx7YJPV8-Cua2dHbMC1S9To3Cfcwff-ykr-IYRJc41mCX_pNA-sKvmpFmd0wPBtgwyCt_tMXuib9LeVuocWRIilgr6OzhmumAAtJCQqEw1bk06F9dNsn`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/data/](https://aides-territoires.beta.gouv.fr/data/)
  
  
  * Method: `GET`
  
  
  * Evidence: `A9es-pour-une-reprise-sur-Aides-territoires`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/](https://aides-territoires.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/serve/MUIEANv2FVIgFOCSUcH4G40Mz7-gNNDCYBU1BnExyPfqcBds83BFiunc-uCZL1sFeaqWrXMAu2qntWXa4I6Y9qxHK1t4nx7YJPV8-Cua2dHbMC1S9To3Cfcwff-ykr-IYRJc41mCX_pNA-sKvmpFmd0wPBtgwyCt_tMXuib9LeVuocWRIilgr6OzhmumAAtJCQqEw1bk06F9dNsn`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/porteurs-aides/](https://aides-territoires.beta.gouv.fr/porteurs-aides/)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/serve/MUIEANv2FVIgFOCSUcH4G40Mz7-gNNDCYBU1BnExyPfqcBds83BFiunc-uCZL1sFeaqWrXMAu2qntWXa4I6Y9qxHK1t4nx7YJPV8-Cua2dHbMC1S9To3Cfcwff-ykr-IYRJc41mCX_pNA-sKvmpFmd0wPBtgwyCt_tMXuib9LeVuocWRIilgr6OzhmumAAtJCQqEw1bk06F9dNsn`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/connexion/](https://aides-territoires.beta.gouv.fr/comptes/connexion/)
  
  
  * Method: `GET`
  
  
  * Evidence: `K6DO2Ujr0ecR7DzcMsNG6huldEestDQKG3uPMnKhm3LzxUWaTqjEznlzf5PAMAEf`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/](https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/broadcast/3105-Aides-Territoires-la-plateforme-qui-permet-aux-territoires-de-trouver-des-aides-pour-financer-et-accompagner-leurs-projets-locaux`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/inscription/](https://aides-territoires.beta.gouv.fr/comptes/inscription/)
  
  
  * Method: `GET`
  
  
  * Evidence: `U8k3gwvqIsouWYaOmzvjEEXAV51OiEPoxf4zdxoNxNuZjlhRNqUUB9pbS96E9k8f`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/contact/](https://aides-territoires.beta.gouv.fr/contact/)
  
  
  * Method: `GET`
  
  
  * Evidence: `U8k3gwvqIsouWYaOmzvjEEXAV51OiEPoxf4zdxoNxNuZjlhRNqUUB9pbS96E9k8f`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/recherche/formulaire/audience/](https://aides-territoires.beta.gouv.fr/recherche/formulaire/audience/)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/serve/MUIEANv2FVIgFOCSUcH4G40Mz7-gNNDCYBU1BnExyPfqcBds83BFiunc-uCZL1sFeaqWrXMAu2qntWXa4I6Y9qxHK1t4nx7YJPV8-Cua2dHbMC1S9To3Cfcwff-ykr-IYRJc41mCX_pNA-sKvmpFmd0wPBtgwyCt_tMXuib9LeVuocWRIilgr6OzhmumAAtJCQqEw1bk06F9dNsn`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr](https://aides-territoires.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/serve/MUIEANv2FVIgFOCSUcH4G40Mz7-gNNDCYBU1BnExyPfqcBds83BFiunc-uCZL1sFeaqWrXMAu2qntWXa4I6Y9qxHK1t4nx7YJPV8-Cua2dHbMC1S9To3Cfcwff-ykr-IYRJc41mCX_pNA-sKvmpFmd0wPBtgwyCt_tMXuib9LeVuocWRIilgr6OzhmumAAtJCQqEw1bk06F9dNsn`
  
  
  
  
Instances: 11
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>~�ۮ��q�-�]}󏀉׬�7��+h������z�~q調���-</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/CACHE/js/output.8a6e3aa6c87c.js](https://aides-territoires.beta.gouv.fr/static/CACHE/js/output.8a6e3aa6c87c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/CACHE/js/output.8a6e3aa6c87c.js](https://aides-territoires.beta.gouv.fr/static/CACHE/js/output.8a6e3aa6c87c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `username`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/CACHE/js/output.8a6e3aa6c87c.js](https://aides-territoires.beta.gouv.fr/static/CACHE/js/output.8a6e3aa6c87c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
Instances: 3
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bFROM\b and was detected 3 times, the first in the element starting with: "if(conv!==true){if(conv&&s.throws){response=conv(response);}else{try{response=conv(response);}catch(e){return{state:"parsererror", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/c131-parcours-de-cybersecurite/](https://aides-territoires.beta.gouv.fr/aides/c131-parcours-de-cybersecurite/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="share-btn" href="#" class="js" data-toggle="modal" data-target="#share-modal">
                Partager cette aide
            </a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/c216-rrr-reemploi-reparation-reutilisation-/](https://aides-territoires.beta.gouv.fr/aides/c216-rrr-reemploi-reparation-reutilisation-/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="share-btn" href="#" class="js" data-toggle="modal" data-target="#share-modal">
                Partager cette aide
            </a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/CACHE/js/output.8a6e3aa6c87c.js](https://aides-territoires.beta.gouv.fr/static/CACHE/js/output.8a6e3aa6c87c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id='"+expando+"'></a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/5442-deployer-les-micro-folies-en-ile-de-france/](https://aides-territoires.beta.gouv.fr/aides/5442-deployer-les-micro-folies-en-ile-de-france/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="share-btn" href="#" class="js" data-toggle="modal" data-target="#share-modal">
                Partager cette aide
            </a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/9d50-copie-12h10-etudier-la-faisabilite-dun-projet/](https://aides-territoires.beta.gouv.fr/aides/9d50-copie-12h10-etudier-la-faisabilite-dun-projet/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="share-btn" href="#" class="js" data-toggle="modal" data-target="#share-modal">
                Partager cette aide
            </a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/2e27-moderniser-les-librairies-aide-a-la-modernisa/](https://aides-territoires.beta.gouv.fr/aides/2e27-moderniser-les-librairies-aide-a-la-modernisa/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="share-btn" href="#" class="js" data-toggle="modal" data-target="#share-modal">
                Partager cette aide
            </a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/e285-norrr-appel-a-projet-pour-financer-des-equipe/](https://aides-territoires.beta.gouv.fr/aides/e285-norrr-appel-a-projet-pour-financer-des-equipe/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="share-btn" href="#" class="js" data-toggle="modal" data-target="#share-modal">
                Partager cette aide
            </a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/8740-reemploiet-reemploi-reutilisation-aide-aux-et/](https://aides-territoires.beta.gouv.fr/aides/8740-reemploiet-reemploi-reutilisation-aide-aux-et/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="share-btn" href="#" class="js" data-toggle="modal" data-target="#share-modal">
                Partager cette aide
            </a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/63c2-recenser-et-evaluer-les-ouvrages-dart-des-pet/](https://aides-territoires.beta.gouv.fr/aides/63c2-recenser-et-evaluer-les-ouvrages-dart-des-pet/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="share-btn" href="#" class="js" data-toggle="modal" data-target="#share-modal">
                Partager cette aide
            </a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/img/logo_RP.svg](https://aides-territoires.beta.gouv.fr/static/img/logo_RP.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script/>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/1185-favoriser-et-developper-les-iniatiatives-perm/](https://aides-territoires.beta.gouv.fr/aides/1185-favoriser-et-developper-les-iniatiatives-perm/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="share-btn" href="#" class="js" data-toggle="modal" data-target="#share-modal">
                Partager cette aide
            </a>`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/8961-copie-10h22-renforcer-le-programme-dhumanisat/](https://aides-territoires.beta.gouv.fr/aides/8961-copie-10h22-renforcer-le-programme-dhumanisat/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="share-btn" href="#" class="js" data-toggle="modal" data-target="#share-modal">
                Partager cette aide
            </a>`
  
  
  
  
Instances: 12
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>Links have been found that do not have traditional href attributes, which is an indication that this is a modern web application.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Non-Storable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are not storable by caching components such as proxy servers. If the response does not contain sensitive, personal or user-specific information, it may benefit from being stored and cached, to improve performance.</p>
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/publications/](https://aides-territoires.beta.gouv.fr/aides/publications/)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/connexion/](https://aides-territoires.beta.gouv.fr/comptes/connexion/)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
Instances: 2
  
### Solution
<p>The content may be marked as storable by ensuring that the following conditions are satisfied:</p><p>The request method must be understood by the cache and defined as being cacheable ("GET", "HEAD", and "POST" are currently defined as cacheable)</p><p>The response status code must be understood by the cache (one of the 1XX, 2XX, 3XX, 4XX, or 5XX response classes are generally understood)</p><p>The "no-store" cache directive must not appear in the request or response header fields</p><p>For caching by "shared" caches such as "proxy" caches, the "private" response directive must not appear in the response</p><p>For caching by "shared" caches such as "proxy" caches, the "Authorization" header field must not appear in the request, unless the response explicitly allows it (using one of the "must-revalidate", "public", or "s-maxage" Cache-Control response directives)</p><p>In addition to the conditions above, at least one of the following conditions must also be satisfied by the response:</p><p>It must contain an "Expires" header field</p><p>It must contain a "max-age" response directive</p><p>For "shared" caches such as "proxy" caches, it must contain a "s-maxage" response directive</p><p>It must contain a "Cache Control Extension" that allows it to be cached</p><p>It must have a status code that is defined as cacheable by default (200, 203, 204, 206, 300, 301, 404, 405, 410, 414, 501).   </p>
  
### Reference
* https://tools.ietf.org/html/rfc7234
* https://tools.ietf.org/html/rfc7231
* http://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html (obsoleted by rfc7234)

  
#### CWE Id : 524
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Storable and Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, and may be retrieved directly from the cache, rather than from the origin server by the caching servers, in response to similar requests from other users.  If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where "shared" caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance.</p>
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/recherche/formulaire/audience/](https://aides-territoires.beta.gouv.fr/recherche/formulaire/audience/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/robots.txt/](https://aides-territoires.beta.gouv.fr/robots.txt/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/](https://aides-territoires.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/](https://aides-territoires.beta.gouv.fr/plateforme-aides-territoires/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/sitemap.xml](https://aides-territoires.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/](https://aides-territoires.beta.gouv.fr/aides-collectivit%C3%A9s/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr](https://aides-territoires.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/porteurs-aides/](https://aides-territoires.beta.gouv.fr/porteurs-aides/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/robots.txt](https://aides-territoires.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
Instances: 9
  
### Solution
<p>Validate that the response does not contain sensitive, personal or user-specific information.  If it does, consider the use of the following HTTP response headers, to limit, or prevent the content being stored and retrieved from the cache by another user:</p><p>Cache-Control: no-cache, no-store, must-revalidate, private</p><p>Pragma: no-cache</p><p>Expires: 0</p><p>This configuration directs both HTTP 1.0 and HTTP 1.1 compliant caching servers to not store the response, and to not retrieve the response (without validation) from the cache, in response to a similar request. </p>
  
### Other information
<p>In the absence of an explicitly specified caching lifetime directive in the response, a liberal lifetime heuristic of 1 year was assumed. This is permitted by rfc7234.</p>
  
### Reference
* https://tools.ietf.org/html/rfc7234
* https://tools.ietf.org/html/rfc7231
* http://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html (obsoleted by rfc7234)

  
#### CWE Id : 524
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Timestamp Disclosure - Unix
##### Informational (Low)
  
  
  
  
#### Description
<p>A timestamp was disclosed by the application/web server - Unix</p>
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/c216-rrr-reemploi-reparation-reutilisation-/](https://aides-territoires.beta.gouv.fr/aides/c216-rrr-reemploi-reparation-reutilisation-/)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/inscription/](https://aides-territoires.beta.gouv.fr/comptes/inscription/)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/static/CACHE/css/output.b74d336c2ebc.css](https://aides-territoires.beta.gouv.fr/static/CACHE/css/output.b74d336c2ebc.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `23009688`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/c216-rrr-reemploi-reparation-reutilisation-/](https://aides-territoires.beta.gouv.fr/aides/c216-rrr-reemploi-reparation-reutilisation-/)
  
  
  * Method: `GET`
  
  
  * Evidence: `76207326`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/comptes/connexion/](https://aides-territoires.beta.gouv.fr/comptes/connexion/)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/5442-deployer-les-micro-folies-en-ile-de-france/](https://aides-territoires.beta.gouv.fr/aides/5442-deployer-les-micro-folies-en-ile-de-france/)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/contact/](https://aides-territoires.beta.gouv.fr/contact/)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/e285-norrr-appel-a-projet-pour-financer-des-equipe/](https://aides-territoires.beta.gouv.fr/aides/e285-norrr-appel-a-projet-pour-financer-des-equipe/)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/2e27-moderniser-les-librairies-aide-a-la-modernisa/](https://aides-territoires.beta.gouv.fr/aides/2e27-moderniser-les-librairies-aide-a-la-modernisa/)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://aides-territoires.beta.gouv.fr/aides/e285-norrr-appel-a-projet-pour-financer-des-equipe/](https://aides-territoires.beta.gouv.fr/aides/e285-norrr-appel-a-projet-pour-financer-des-equipe/)
  
  
  * Method: `GET`
  
  
  * Evidence: `20210419`
  
  
  
  
Instances: 10
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>31449600, which evaluates to: 1970-12-31 00:00:00</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3