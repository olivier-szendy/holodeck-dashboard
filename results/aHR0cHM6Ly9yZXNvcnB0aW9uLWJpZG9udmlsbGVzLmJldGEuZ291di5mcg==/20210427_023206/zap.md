
# ZAP Scanning Report

Generated on Tue, 27 Apr 2021 02:26:53


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 2 |
| Low | 5 |
| Informational | 5 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 4 | 
| X-Frame-Options Header Not Set | Medium | 4 | 
| Dangerous JS Functions | Low | 2 | 
| Feature Policy Header Not Set | Low | 6 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 6 | 
| Server Leaks Version Information via "Server" HTTP Response Header Field | Low | 9 | 
| X-Content-Type-Options Header Missing | Low | 9 | 
| Base64 Disclosure | Informational | 2 | 
| Information Disclosure - Suspicious Comments | Informational | 10 | 
| Modern Web Application | Informational | 6 | 
| Storable and Cacheable Content | Informational | 9 | 
| Timestamp Disclosure - Unix | Informational | 13 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr](https://resorption-bidonvilles.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/robots.txt](https://resorption-bidonvilles.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/](https://resorption-bidonvilles.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/sitemap.xml](https://resorption-bidonvilles.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
Instances: 4
  
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

  
  
  
  
### X-Frame-Options Header Not Set
##### Medium (Medium)
  
  
  
  
#### Description
<p>X-Frame-Options header is not included in the HTTP response to protect against 'ClickJacking' attacks.</p>
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/robots.txt](https://resorption-bidonvilles.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/](https://resorption-bidonvilles.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr](https://resorption-bidonvilles.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/sitemap.xml](https://resorption-bidonvilles.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
Instances: 4
  
### Solution
<p>Most modern Web browsers support the X-Frame-Options HTTP header. Ensure it's set on all web pages returned by your site (if you expect the page to be framed only by pages on your server (e.g. it's part of a FRAMESET) then you'll want to use SAMEORIGIN, otherwise if you never expect the page to be framed, you should use DENY. Alternatively consider implementing Content Security Policy's "frame-ancestors" directive. </p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Dangerous JS Functions
##### Low (Low)
  
  
  
  
#### Description
<p>A dangerous JS function seems to be in use that would leave the site vulnerable.</p>
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js](https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/js/index.f644ce68.js](https://resorption-bidonvilles.beta.gouv.fr/js/index.f644ce68.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
Instances: 2
  
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
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js](https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/robots.txt](https://resorption-bidonvilles.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/sitemap.xml](https://resorption-bidonvilles.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr](https://resorption-bidonvilles.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/](https://resorption-bidonvilles.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/js/index.f644ce68.js](https://resorption-bidonvilles.beta.gouv.fr/js/index.f644ce68.js)
  
  
  * Method: `GET`
  
  
  
  
Instances: 6
  
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
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/robots.txt](https://resorption-bidonvilles.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/sitemap.xml](https://resorption-bidonvilles.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr](https://resorption-bidonvilles.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/](https://resorption-bidonvilles.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/css/chunk-vendors.da349212.css](https://resorption-bidonvilles.beta.gouv.fr/css/chunk-vendors.da349212.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/css/index.5be93f44.css](https://resorption-bidonvilles.beta.gouv.fr/css/index.5be93f44.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
Instances: 6
  
### Solution
<p>Whenever possible ensure the cache-control HTTP header is set with no-cache, no-store, must-revalidate; and that the pragma HTTP header is set with no-cache.</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching

  
#### CWE Id : 525
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Server Leaks Version Information via "Server" HTTP Response Header Field
##### Low (High)
  
  
  
  
#### Description
<p>The web/application server is leaking version information via the "Server" HTTP response header. Access to such information may facilitate attackers identifying other vulnerabilities your web/application server is subject to.</p>
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js](https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.19.10`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr](https://resorption-bidonvilles.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.19.10`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/robots.txt](https://resorption-bidonvilles.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.19.10`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/](https://resorption-bidonvilles.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.19.10`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/js/index.f644ce68.js](https://resorption-bidonvilles.beta.gouv.fr/js/index.f644ce68.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.19.10`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/img/favicon.ico](https://resorption-bidonvilles.beta.gouv.fr/img/favicon.ico)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.19.10`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/css/chunk-vendors.da349212.css](https://resorption-bidonvilles.beta.gouv.fr/css/chunk-vendors.da349212.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.19.10`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/css/index.5be93f44.css](https://resorption-bidonvilles.beta.gouv.fr/css/index.5be93f44.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.19.10`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/sitemap.xml](https://resorption-bidonvilles.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.19.10`
  
  
  
  
Instances: 9
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to suppress the "Server" header or provide generic details.</p>
  
### Reference
* http://httpd.apache.org/docs/current/mod/core.html#servertokens
* http://msdn.microsoft.com/en-us/library/ff648552.aspx#ht_urlscan_007
* http://blogs.msdn.com/b/varunm/archive/2013/04/23/remove-unwanted-http-response-headers.aspx
* http://www.troyhunt.com/2012/02/shhh-dont-let-your-response-headers.html

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### X-Content-Type-Options Header Missing
##### Low (Medium)
  
  
  
  
#### Description
<p>The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.</p>
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/js/index.f644ce68.js](https://resorption-bidonvilles.beta.gouv.fr/js/index.f644ce68.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/](https://resorption-bidonvilles.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js](https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/robots.txt](https://resorption-bidonvilles.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr](https://resorption-bidonvilles.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/css/index.5be93f44.css](https://resorption-bidonvilles.beta.gouv.fr/css/index.5be93f44.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/css/chunk-vendors.da349212.css](https://resorption-bidonvilles.beta.gouv.fr/css/chunk-vendors.da349212.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/img/favicon.ico](https://resorption-bidonvilles.beta.gouv.fr/img/favicon.ico)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/sitemap.xml](https://resorption-bidonvilles.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
Instances: 9
  
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
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js](https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `416H64v-96h160v96zm0-160H64v-96h160v96zm224`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/js/index.f644ce68.js](https://resorption-bidonvilles.beta.gouv.fr/js/index.f644ce68.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `indexOfHighlightedSuggestion-1`
  
  
  
  
Instances: 2
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�^�����u�K��9��^�\x001f�/�ޡ׭/����n</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js](https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js](https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js](https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `db`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js](https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `XXX`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/js/index.f644ce68.js](https://resorption-bidonvilles.beta.gouv.fr/js/index.f644ce68.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js](https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `username`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js](https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `bug`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js](https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js](https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `where`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js](https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
Instances: 10
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bFROM\b and was detected 17 times, the first in the element starting with: "function e(t){return t%100===11||t%10!==1}function n(t,n,r,i){var a=t+" ";switch(r){case"s":return n||i?"nokkrar sekúndur":"nokk", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js](https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a>")})),c=function(){return"$0"==="a".replace(/./,"$0")}(),d=a("replace"),h=function(){return!!/./[d]&&""===/./[d]("a","$0")}(),f=!i((function(){var t=/(?:)/,e=t.exec;t.exec=function(){return e.apply(this,arguments)};var n="ab".split(t);return 2!==n.length||"a"!==n[0]||"b"!==n[1]}));t.exports=function(t,e,n,d){var p=a(t),m=!i((function(){var e={};return e[p]=function(){return 7},7!=""[t](e)})),_=m&&!i((function(){var e=!1,n=/a/;return"split"===t&&(n={},n.constructor={},n.constructor[u]=function(){return n},n.flags="",n[p]=/./[p]),n.exec=function(){return e=!0,null},n[p](""),!e}));if(!m||!_||"replace"===t&&(!l||!c||h)||"split"===t&&!f){var v=/./[p],g=n(p,""[t],(function(t,e,n,r,i){return e.exec===o?m&&!i?{done:!0,value:v.call(e,n,r)}:{done:!0,value:t.call(n,e,r)}:{done:!1}}),{REPLACE_KEEPS_$0:c,REGEXP_REPLACE_SUBSTITUTES_UNDEFINED_CAPTURE:h}),y=g[0],b=g[1];r(String.prototype,t,y),r(RegExp.prototype,p,2==e?function(t,e){return b.call(t,this,e)}:function(t){return b.call(t,this)})}d&&s(RegExp.prototype[p],"sham",!0)}},d80f:function(t,e,n){var r=n("23e7"),i=n("fc6a"),a=n("50c4");r({target:"String",stat:!0},{raw:function(t){var e=i(t.raw),n=a(e.length),r=arguments.length,o=[],s=0;while(n>s)o.push(String(e[s++])),s<r&&o.push(String(arguments[s]));return o.join("")}})},d81d:function(t,e,n){"use strict";var r=n("23e7"),i=n("b727").map,a=n("1dde"),o=a("map");r({target:"Array",proto:!0,forced:!o},{map:function(t){return i(this,t,arguments.length>1?arguments[1]:void 0)}})},d9f8:function(t,e,n){(function(t,e){e(n("c1df"))})(0,(function(t){"use strict";
//! moment.js locale configuration
var e=t.defineLocale("fr-ca",{months:"janvier_février_mars_avril_mai_juin_juillet_août_septembre_octobre_novembre_décembre".split("_"),monthsShort:"janv._févr._mars_avr._mai_juin_juil._août_sept._oct._nov._déc.".split("_"),monthsParseExact:!0,weekdays:"dimanche_lundi_mardi_mercredi_jeudi_vendredi_samedi".split("_"),weekdaysShort:"dim._lun._mar._mer._jeu._ven._sam.".split("_"),weekdaysMin:"di_lu_ma_me_je_ve_sa".split("_"),weekdaysParseExact:!0,longDateFormat:{LT:"HH:mm",LTS:"HH:mm:ss",L:"YYYY-MM-DD",LL:"D MMMM YYYY",LLL:"D MMMM YYYY HH:mm",LLLL:"dddd D MMMM YYYY HH:mm"},calendar:{sameDay:"[Aujourd’hui à] LT",nextDay:"[Demain à] LT",nextWeek:"dddd [à] LT",lastDay:"[Hier à] LT",lastWeek:"dddd [dernier à] LT",sameElse:"L"},relativeTime:{future:"dans %s",past:"il y a %s",s:"quelques secondes",ss:"%d secondes",m:"une minute",mm:"%d minutes",h:"une heure",hh:"%d heures",d:"un jour",dd:"%d jours",M:"un mois",MM:"%d mois",y:"un an",yy:"%d ans"},dayOfMonthOrdinalParse:/\d{1,2}(er|e)/,ordinal:function(t,e){switch(e){default:case"M":case"Q":case"D":case"DDD":case"d":return t+(1===t?"er":"e");case"w":case"W":return t+(1===t?"re":"e")}}});return e}))},da84:function(t,e,n){(function(e){var n=function(t){return t&&t.Math==Math&&t};t.exports=n("object"==typeof globalThis&&globalThis)||n("object"==typeof window&&window)||n("object"==typeof self&&self)||n("object"==typeof e&&e)||function(){return this}()||Function("return this")()}).call(this,n("c8ba"))},dac4:function(t,e,n){},db29:function(t,e,n){(function(t,e){e(n("c1df"))})(0,(function(t){"use strict";
//! moment.js locale configuration
var e="jan._feb._mrt._apr._mei_jun._jul._aug._sep._okt._nov._dec.".split("_"),n="jan_feb_mrt_apr_mei_jun_jul_aug_sep_okt_nov_dec".split("_"),r=[/^jan/i,/^feb/i,/^maart|mrt.?$/i,/^apr/i,/^mei$/i,/^jun[i.]?$/i,/^jul[i.]?$/i,/^aug/i,/^sep/i,/^okt/i,/^nov/i,/^dec/i],i=/^(januari|februari|maart|april|mei|ju[nl]i|augustus|september|oktober|november|december|jan\.?|feb\.?|mrt\.?|apr\.?|ju[nl]\.?|aug\.?|sep\.?|okt\.?|nov\.?|dec\.?)/i,a=t.defineLocale("nl-be",{months:"januari_februari_maart_april_mei_juni_juli_augustus_september_oktober_november_december".split("_"),monthsShort:function(t,r){return t?/-MMM-/.test(r)?n[t.month()]:e[t.month()]:e},monthsRegex:i,monthsShortRegex:i,monthsStrictRegex:/^(januari|februari|maart|april|mei|ju[nl]i|augustus|september|oktober|november|december)/i,monthsShortStrictRegex:/^(jan\.?|feb\.?|mrt\.?|apr\.?|mei|ju[nl]\.?|aug\.?|sep\.?|okt\.?|nov\.?|dec\.?)/i,monthsParse:r,longMonthsParse:r,shortMonthsParse:r,weekdays:"zondag_maandag_dinsdag_woensdag_donderdag_vrijdag_zaterdag".split("_"),weekdaysShort:"zo._ma._di._wo._do._vr._za.".split("_"),weekdaysMin:"zo_ma_di_wo_do_vr_za".split("_"),weekdaysParseExact:!0,longDateFormat:{LT:"HH:mm",LTS:"HH:mm:ss",L:"DD/MM/YYYY",LL:"D MMMM YYYY",LLL:"D MMMM YYYY HH:mm",LLLL:"dddd D MMMM YYYY HH:mm"},calendar:{sameDay:"[vandaag om] LT",nextDay:"[morgen om] LT",nextWeek:"dddd [om] LT",lastDay:"[gisteren om] LT",lastWeek:"[afgelopen] dddd [om] LT",sameElse:"L"},relativeTime:{future:"over %s",past:"%s geleden",s:"een paar seconden",ss:"%d seconden",m:"één minuut",mm:"%d minuten",h:"één uur",hh:"%d uur",d:"één dag",dd:"%d dagen",M:"één maand",MM:"%d maanden",y:"één jaar",yy:"%d jaar"},dayOfMonthOrdinalParse:/\d{1,2}(ste|de)/,ordinal:function(t){return t+(1===t||8===t||t>=20?"ste":"de")},week:{dow:1,doy:4}});return a}))},db96:function(t,e,n){var r=n("23e7"),i=n("825a"),a=Object.isExtensible;r({target:"Reflect",stat:!0},{isExtensible:function(t){return i(t),!a||a(t)}})},dbb4:function(t,e,n){var r=n("23e7"),i=n("83ab"),a=n("56ef"),o=n("fc6a"),s=n("06cf"),u=n("8418");r({target:"Object",stat:!0,sham:!i},{getOwnPropertyDescriptors:function(t){var e,n,r=o(t),i=s.f,l=a(r),c={},d=0;while(l.length>d)n=i(r,e=l[d++]),void 0!==n&&u(c,e,n);return c}})},dbfa:function(t,e,n){"use strict";var r=n("23e7"),i=n("1c0b"),a=n("d066"),o=n("f069"),s=n("e667"),u=n("2266"),l="No one promise resolved";r({target:"Promise",stat:!0},{any:function(t){var e=this,n=o.f(e),r=n.resolve,c=n.reject,d=s((function(){var n=i(e.resolve),o=[],s=0,d=1,h=!1;u(t,(function(t){var i=s++,u=!1;o.push(void 0),d++,n.call(e,t).then((function(t){u||h||(h=!0,r(t))}),(function(t){u||h||(u=!0,o[i]=t,--d||c(new(a("AggregateError"))(o,l)))}))})),--d||c(new(a("AggregateError"))(o,l))}));return d.error&&c(d.value),n.promise}})},dc4d:function(t,e,n){(function(t,e){e(n("c1df"))})(0,(function(t){"use strict";
//! moment.js locale configuration
var e={1:"१",2:"२",3:"३",4:"४",5:"५",6:"६",7:"७",8:"८",9:"९",0:"०"},n={"१":"1","२":"2","३":"3","४":"4","५":"5","६":"6","७":"7","८":"8","९":"9","०":"0"},r=[/^जन/i,/^फ़र|फर/i,/^मार्च/i,/^अप्रै/i,/^मई/i,/^जून/i,/^जुल/i,/^अग/i,/^सितं|सित/i,/^अक्टू/i,/^नव|नवं/i,/^दिसं|दिस/i],i=[/^जन/i,/^फ़र/i,/^मार्च/i,/^अप्रै/i,/^मई/i,/^जून/i,/^जुल/i,/^अग/i,/^सित/i,/^अक्टू/i,/^नव/i,/^दिस/i],a=t.defineLocale("hi",{months:{format:"जनवरी_फ़रवरी_मार्च_अप्रैल_मई_जून_जुलाई_अगस्त_सितम्बर_अक्टूबर_नवम्बर_दिसम्बर".split("_"),standalone:"जनवरी_फरवरी_मार्च_अप्रैल_मई_जून_जुलाई_अगस्त_सितंबर_अक्टूबर_नवंबर_दिसंबर".split("_")},monthsShort:"जन._फ़र._मार्च_अप्रै._मई_जून_जुल._अग._सित._अक्टू._नव._दिस.".split("_"),weekdays:"रविवार_सोमवार_मंगलवार_बुधवार_गुरूवार_शुक्रवार_शनिवार".split("_"),weekdaysShort:"रवि_सोम_मंगल_बुध_गुरू_शुक्र_शनि".split("_"),weekdaysMin:"र_सो_मं_बु_गु_शु_श".split("_"),longDateFormat:{LT:"A h:mm बजे",LTS:"A h:mm:ss बजे",L:"DD/MM/YYYY",LL:"D MMMM YYYY",LLL:"D MMMM YYYY, A h:mm बजे",LLLL:"dddd, D MMMM YYYY, A h:mm बजे"},monthsParse:r,longMonthsParse:r,shortMonthsParse:i,monthsRegex:/^(जनवरी|जन\.?|फ़रवरी|फरवरी|फ़र\.?|मार्च?|अप्रैल|अप्रै\.?|मई?|जून?|जुलाई|जुल\.?|अगस्त|अग\.?|सितम्बर|सितंबर|सित\.?|अक्टूबर|अक्टू\.?|नवम्बर|नवंबर|नव\.?|दिसम्बर|दिसंबर|दिस\.?)/i,monthsShortRegex:/^(जनवरी|जन\.?|फ़रवरी|फरवरी|फ़र\.?|मार्च?|अप्रैल|अप्रै\.?|मई?|जून?|जुलाई|जुल\.?|अगस्त|अग\.?|सितम्बर|सितंबर|सित\.?|अक्टूबर|अक्टू\.?|नवम्बर|नवंबर|नव\.?|दिसम्बर|दिसंबर|दिस\.?)/i,monthsStrictRegex:/^(जनवरी?|फ़रवरी|फरवरी?|मार्च?|अप्रैल?|मई?|जून?|जुलाई?|अगस्त?|सितम्बर|सितंबर|सित?\.?|अक्टूबर|अक्टू\.?|नवम्बर|नवंबर?|दिसम्बर|दिसंबर?)/i,monthsShortStrictRegex:/^(जन\.?|फ़र\.?|मार्च?|अप्रै\.?|मई?|जून?|जुल\.?|अग\.?|सित\.?|अक्टू\.?|नव\.?|दिस\.?)/i,calendar:{sameDay:"[आज] LT",nextDay:"[कल] LT",nextWeek:"dddd, LT",lastDay:"[कल] LT",lastWeek:"[पिछले] dddd, LT",sameElse:"L"},relativeTime:{future:"%s में",past:"%s पहले",s:"कुछ ही क्षण",ss:"%d सेकंड",m:"एक मिनट",mm:"%d मिनट",h:"एक घंटा",hh:"%d घंटे",d:"एक दिन",dd:"%d दिन",M:"एक महीने",MM:"%d महीने",y:"एक वर्ष",yy:"%d वर्ष"},preparse:function(t){return t.replace(/[१२३४५६७८९०]/g,(function(t){return n[t]}))},postformat:function(t){return t.replace(/\d/g,(function(t){return e[t]}))},meridiemParse:/रात|सुबह|दोपहर|शाम/,meridiemHour:function(t,e){return 12===t&&(t=0),"रात"===e?t<4?t:t+12:"सुबह"===e?t:"दोपहर"===e?t>=10?t:t+12:"शाम"===e?t+12:void 0},meridiem:function(t,e,n){return t<4?"रात":t<10?"सुबह":t<17?"दोपहर":t<20?"शाम":"रात"},week:{dow:0,doy:6}});return a}))},dc8d:function(t,e,n){var r=n("746f");r("hasInstance")},dca8:function(t,e,n){var r=n("23e7"),i=n("bb2f"),a=n("d039"),o=n("861d"),s=n("f183").onFreeze,u=Object.freeze,l=a((function(){u(1)}));r({target:"Object",stat:!0,forced:l,sham:!i},{freeze:function(t){return u&&o(t)?u(s(t)):t}})},dd40:function(t,e){t.exports=function(t){if(!t.webpackPolyfill){var e=Object.create(t);e.children||(e.children=[]),Object.defineProperty(e,"loaded",{enumerable:!0,get:function(){return e.l}}),Object.defineProperty(e,"id",{enumerable:!0,get:function(){return e.i}}),Object.defineProperty(e,"exports",{enumerable:!0}),e.webpackPolyfill=1}return e}},ddb0:function(t,e,n){var r=n("da84"),i=n("fdbc"),a=n("e260"),o=n("9112"),s=n("b622"),u=s("iterator"),l=s("toStringTag"),c=a.values;for(var d in i){var h=r[d],f=h&&h.prototype;if(f){if(f[u]!==c)try{o(f,u,c)}catch(m){f[u]=c}if(f[l]||o(f,l,d),i[d])for(var p in a)if(f[p]!==a[p])try{o(f,p,a[p])}catch(m){f[p]=a[p]}}}},df75:function(t,e,n){var r=n("ca84"),i=n("7839");t.exports=Object.keys||function(t){return r(t,i)}},df7c:function(t,e,n){(function(t){function n(t,e){for(var n=0,r=t.length-1;r>=0;r--){var i=t[r];"."===i?t.splice(r,1):".."===i?(t.splice(r,1),n++):n&&(t.splice(r,1),n--)}if(e)for(;n--;n)t.unshift("..");return t}function r(t){"string"!==typeof t&&(t+="");var e,n=0,r=-1,i=!0;for(e=t.length-1;e>=0;--e)if(47===t.charCodeAt(e)){if(!i){n=e+1;break}}else-1===r&&(i=!1,r=e+1);return-1===r?"":t.slice(n,r)}function i(t,e){if(t.filter)return t.filter(e);for(var n=[],r=0;r<t.length;r++)e(t[r],r,t)&&n.push(t[r]);return n}e.resolve=function(){for(var e="",r=!1,a=arguments.length-1;a>=-1&&!r;a--){var o=a>=0?arguments[a]:t.cwd();if("string"!==typeof o)throw new TypeError("Arguments to path.resolve must be strings");o&&(e=o+"/"+e,r="/"===o.charAt(0))}return e=n(i(e.split("/"),(function(t){return!!t})),!r).join("/"),(r?"/":"")+e||"."},e.normalize=function(t){var r=e.isAbsolute(t),o="/"===a(t,-1);return t=n(i(t.split("/"),(function(t){return!!t})),!r).join("/"),t||r||(t="."),t&&o&&(t+="/"),(r?"/":"")+t},e.isAbsolute=function(t){return"/"===t.charAt(0)},e.join=function(){var t=Array.prototype.slice.call(arguments,0);return e.normalize(i(t,(function(t,e){if("string"!==typeof t)throw new TypeError("Arguments to path.join must be strings");return t})).join("/"))},e.relative=function(t,n){function r(t){for(var e=0;e<t.length;e++)if(""!==t[e])break;for(var n=t.length-1;n>=0;n--)if(""!==t[n])break;return e>n?[]:t.slice(e,n-e+1)}t=e.resolve(t).substr(1),n=e.resolve(n).substr(1);for(var i=r(t.split("/")),a=r(n.split("/")),o=Math.min(i.length,a.length),s=o,u=0;u<o;u++)if(i[u]!==a[u]){s=u;break}var l=[];for(u=s;u<i.length;u++)l.push("..");return l=l.concat(a.slice(s)),l.join("/")},e.sep="/",e.delimiter=":",e.dirname=function(t){if("string"!==typeof t&&(t+=""),0===t.length)return".";for(var e=t.charCodeAt(0),n=47===e,r=-1,i=!0,a=t.length-1;a>=1;--a)if(e=t.charCodeAt(a),47===e){if(!i){r=a;break}}else i=!1;return-1===r?n?"/":".":n&&1===r?"/":t.slice(0,r)},e.basename=function(t,e){var n=r(t);return e&&n.substr(-1*e.length)===e&&(n=n.substr(0,n.length-e.length)),n},e.extname=function(t){"string"!==typeof t&&(t+="");for(var e=-1,n=0,r=-1,i=!0,a=0,o=t.length-1;o>=0;--o){var s=t.charCodeAt(o);if(47!==s)-1===r&&(i=!1,r=o+1),46===s?-1===e?e=o:1!==a&&(a=1):-1!==e&&(a=-1);else if(!i){n=o+1;break}}return-1===e||-1===r||0===a||1===a&&e===r-1&&e===n+1?"":t.slice(e,r)};var a="b"==="ab".substr(-1)?function(t,e,n){return t.substr(e,n)}:function(t,e,n){return e<0&&(e=t.length+e),t.substr(e,n)}}).call(this,n("4362"))},e01a:function(t,e,n){"use strict";var r=n("23e7"),i=n("83ab"),a=n("da84"),o=n("5135"),s=n("861d"),u=n("9bf2").f,l=n("e893"),c=a.Symbol;if(i&&"function"==typeof c&&(!("description"in c.prototype)||void 0!==c().description)){var d={},h=function(){var t=arguments.length<1||void 0===arguments[0]?void 0:String(arguments[0]),e=this instanceof h?new c(t):void 0===t?c():c(t);return""===t&&(d[e]=!0),e};l(h,c);var f=h.prototype=c.prototype;f.constructor=h;var p=f.toString,m="Symbol(test)"==String(c("test")),_=/^Symbol\((.*)\)[^)]+$/;u(f,"description",{configurable:!0,get:function(){var t=s(this)?this.valueOf():this,e=p.call(t);if(o(d,t))return"";var n=m?e.slice(7,-1):e.replace(_,"$1");return""===n?void 0:n}}),r({global:!0,forced:!0},{Symbol:h})}},e0c5:function(t,e,n){(function(t,e){e(n("c1df"))})(0,(function(t){"use strict";
//! moment.js locale configuration
var e={1:"૧",2:"૨",3:"૩",4:"૪",5:"૫",6:"૬",7:"૭",8:"૮",9:"૯",0:"૦"},n={"૧":"1","૨":"2","૩":"3","૪":"4","૫":"5","૬":"6","૭":"7","૮":"8","૯":"9","૦":"0"},r=t.defineLocale("gu",{months:"જાન્યુઆરી_ફેબ્રુઆરી_માર્ચ_એપ્રિલ_મે_જૂન_જુલાઈ_ઑગસ્ટ_સપ્ટેમ્બર_ઑક્ટ્બર_નવેમ્બર_ડિસેમ્બર".split("_"),monthsShort:"જાન્યુ._ફેબ્રુ._માર્ચ_એપ્રિ._મે_જૂન_જુલા._ઑગ._સપ્ટે._ઑક્ટ્._નવે._ડિસે.".split("_"),monthsParseExact:!0,weekdays:"રવિવાર_સોમવાર_મંગળવાર_બુધ્વાર_ગુરુવાર_શુક્રવાર_શનિવાર".split("_"),weekdaysShort:"રવિ_સોમ_મંગળ_બુધ્_ગુરુ_શુક્ર_શનિ".split("_"),weekdaysMin:"ર_સો_મં_બુ_ગુ_શુ_શ".split("_"),longDateFormat:{LT:"A h:mm વાગ્યે",LTS:"A h:mm:ss વાગ્યે",L:"DD/MM/YYYY",LL:"D MMMM YYYY",LLL:"D MMMM YYYY, A h:mm વાગ્યે",LLLL:"dddd, D MMMM YYYY, A h:mm વાગ્યે"},calendar:{sameDay:"[આજ] LT",nextDay:"[કાલે] LT",nextWeek:"dddd, LT",lastDay:"[ગઇકાલે] LT",lastWeek:"[પાછલા] dddd, LT",sameElse:"L"},relativeTime:{future:"%s મા",past:"%s પહેલા",s:"અમુક પળો",ss:"%d સેકંડ",m:"એક મિનિટ",mm:"%d મિનિટ",h:"એક કલાક",hh:"%d કલાક",d:"એક દિવસ",dd:"%d દિવસ",M:"એક મહિનો",MM:"%d મહિનો",y:"એક વર્ષ",yy:"%d વર્ષ"},preparse:function(t){return t.replace(/[૧૨૩૪૫૬૭૮૯૦]/g,(function(t){return n[t]}))},postformat:function(t){return t.replace(/\d/g,(function(t){return e[t]}))},meridiemParse:/રાત|બપોર|સવાર|સાંજ/,meridiemHour:function(t,e){return 12===t&&(t=0),"રાત"===e?t<4?t:t+12:"સવાર"===e?t:"બપોર"===e?t>=10?t:t+12:"સાંજ"===e?t+12:void 0},meridiem:function(t,e,n){return t<4?"રાત":t<10?"સવાર":t<17?"બપોર":t<20?"સાંજ":"રાત"},week:{dow:0,doy:6}});return r}))},e11e:function(t,e,n){
/* @preserve
 * Leaflet 1.7.1, a JS library for interactive maps. http://leafletjs.com
 * (c) 2010-2019 Vladimir Agafonkin, (c) 2010-2011 CloudMade
 */
(function(t,n){n(e)})(0,(function(t){"use strict";var e="1.7.1";function n(t){var e,n,r,i;for(n=1,r=arguments.length;n<r;n++)for(e in i=arguments[n],i)t[e]=i[e];return t}var r=Object.create||function(){function t(){}return function(e){return t.prototype=e,new t}}();function i(t,e){var n=Array.prototype.slice;if(t.bind)return t.bind.apply(t,n.call(arguments,1));var r=n.call(arguments,2);return function(){return t.apply(e,r.length?r.concat(n.call(arguments)):arguments)}}var a=0;function o(t){return t._leaflet_id=t._leaflet_id||++a,t._leaflet_id}function s(t,e,n){var r,i,a,o;return o=function(){r=!1,i&&(a.apply(n,i),i=!1)},a=function(){r?i=arguments:(t.apply(n,arguments),setTimeout(o,e),r=!0)},a}function u(t,e,n){var r=e[1],i=e[0],a=r-i;return t===r&&n?t:((t-i)%a+a)%a+i}function l(){return!1}function c(t,e){var n=Math.pow(10,void 0===e?6:e);return Math.round(t*n)/n}function d(t){return t.trim?t.trim():t.replace(/^\s+|\s+$/g,"")}function h(t){return d(t).split(/\s+/)}function f(t,e){for(var n in Object.prototype.hasOwnProperty.call(t,"options")||(t.options=t.options?r(t.options):{}),e)t.options[n]=e[n];return t.options}function p(t,e,n){var r=[];for(var i in t)r.push(encodeURIComponent(n?i.toUpperCase():i)+"="+encodeURIComponent(t[i]));return(e&&-1!==e.indexOf("?")?"&":"?")+r.join("&")}var m=/\{ *([\w_-]+) *\}/g;function _(t,e){return t.replace(m,(function(t,n){var r=e[n];if(void 0===r)throw new Error("No value provided for variable "+t);return"function"===typeof r&&(r=r(e)),r}))}var v=Array.isArray||function(t){return"[object Array]"===Object.prototype.toString.call(t)};function g(t,e){for(var n=0;n<t.length;n++)if(t[n]===e)return n;return-1}var y="data:image/gif;base64,R0lGODlhAQABAAD/ACwAAAAAAQABAAACADs=";function b(t){return window["webkit"+t]||window["moz"+t]||window["ms"+t]}var w=0;function M(t){var e=+new Date,n=Math.max(0,16-(e-w));return w=e+n,window.setTimeout(t,n)}var x=window.requestAnimationFrame||b("RequestAnimationFrame")||M,k=window.cancelAnimationFrame||b("CancelAnimationFrame")||b("CancelRequestAnimationFrame")||function(t){window.clearTimeout(t)};function T(t,e,n){if(!n||x!==M)return x.call(window,i(t,e));t.call(e)}function S(t){t&&k.call(window,t)}var D={extend:n,create:r,bind:i,lastId:a,stamp:o,throttle:s,wrapNum:u,falseFn:l,formatNum:c,trim:d,splitWords:h,setOptions:f,getParamString:p,template:_,isArray:v,indexOf:g,emptyImageUrl:y,requestFn:x,cancelFn:k,requestAnimFrame:T,cancelAnimFrame:S};function Y(){}function O(t){if("undefined"!==typeof L&&L&&L.Mixin){t=v(t)?t:[t];for(var e=0;e<t.length;e++)t[e]===L.Mixin.Events&&console.warn("Deprecated include of L.Mixin.Events: this property will be removed in future releases, please inherit from L.Evented instead.",(new Error).stack)}}Y.extend=function(t){var e=function(){this.initialize&&this.initialize.apply(this,arguments),this.callInitHooks()},i=e.__super__=this.prototype,a=r(i);for(var o in a.constructor=e,e.prototype=a,this)Object.prototype.hasOwnProperty.call(this,o)&&"prototype"!==o&&"__super__"!==o&&(e[o]=this[o]);return t.statics&&(n(e,t.statics),delete t.statics),t.includes&&(O(t.includes),n.apply(null,[a].concat(t.includes)),delete t.includes),a.options&&(t.options=n(r(a.options),t.options)),n(a,t),a._initHooks=[],a.callInitHooks=function(){if(!this._initHooksCalled){i.callInitHooks&&i.callInitHooks.call(this),this._initHooksCalled=!0;for(var t=0,e=a._initHooks.length;t<e;t++)a._initHooks[t].call(this)}},e},Y.include=function(t){return n(this.prototype,t),this},Y.mergeOptions=function(t){return n(this.prototype.options,t),this},Y.addInitHook=function(t){var e=Array.prototype.slice.call(arguments,1),n="function"===typeof t?t:function(){this[t].apply(this,e)};return this.prototype._initHooks=this.prototype._initHooks||[],this.prototype._initHooks.push(n),this};var A={on:function(t,e,n){if("object"===typeof t)for(var r in t)this._on(r,t[r],e);else{t=h(t);for(var i=0,a=t.length;i<a;i++)this._on(t[i],e,n)}return this},off:function(t,e,n){if(t)if("object"===typeof t)for(var r in t)this._off(r,t[r],e);else{t=h(t);for(var i=0,a=t.length;i<a;i++)this._off(t[i],e,n)}else delete this._events;return this},_on:function(t,e,n){this._events=this._events||{};var r=this._events[t];r||(r=[],this._events[t]=r),n===this&&(n=void 0);for(var i={fn:e,ctx:n},a=r,o=0,s=a.length;o<s;o++)if(a[o].fn===e&&a[o].ctx===n)return;a.push(i)},_off:function(t,e,n){var r,i,a;if(this._events&&(r=this._events[t],r))if(e){if(n===this&&(n=void 0),r)for(i=0,a=r.length;i<a;i++){var o=r[i];if(o.ctx===n&&o.fn===e)return o.fn=l,this._firingCount&&(this._events[t]=r=r.slice()),void r.splice(i,1)}}else{for(i=0,a=r.length;i<a;i++)r[i].fn=l;delete this._events[t]}},fire:function(t,e,r){if(!this.listens(t,r))return this;var i=n({},e,{type:t,target:this,sourceTarget:e&&e.sourceTarget||this});if(this._events){var a=this._events[t];if(a){this._firingCount=this._firingCount+1||1;for(var o=0,s=a.length;o<s;o++){var u=a[o];u.fn.call(u.ctx||this,i)}this._firingCount--}}return r&&this._propagateEvent(i),this},listens:function(t,e){var n=this._events&&this._events[t];if(n&&n.length)return!0;if(e)for(var r in this._eventParents)if(this._eventParents[r].listens(t,e))return!0;return!1},once:function(t,e,n){if("object"===typeof t){for(var r in t)this.once(r,t[r],e);return this}var a=i((function(){this.off(t,e,n).off(t,a,n)}),this);return this.on(t,e,n).on(t,a,n)},addEventParent:function(t){return this._eventParents=this._eventParents||{},this._eventParents[o(t)]=t,this},removeEventParent:function(t){return this._eventParents&&delete this._eventParents[o(t)],this},_propagateEvent:function(t){for(var e in this._eventParents)this._eventParents[e].fire(t.type,n({layer:t.target,propagatedFrom:t.target},t),!0)}};A.addEventListener=A.on,A.removeEventListener=A.clearAllEventListeners=A.off,A.addOneTimeEventListener=A.once,A.fireEvent=A.fire,A.hasEventListeners=A.listens;var C=Y.extend(A);function P(t,e,n){this.x=n?Math.round(t):t,this.y=n?Math.round(e):e}var E=Math.trunc||function(t){return t>0?Math.floor(t):Math.ceil(t)};function j(t,e,n){return t instanceof P?t:v(t)?new P(t[0],t[1]):void 0===t||null===t?t:"object"===typeof t&&"x"in t&&"y"in t?new P(t.x,t.y):new P(t,e,n)}function H(t,e){if(t)for(var n=e?[t,e]:t,r=0,i=n.length;r<i;r++)this.extend(n[r])}function I(t,e){return!t||t instanceof H?t:new H(t,e)}function R(t,e){if(t)for(var n=e?[t,e]:t,r=0,i=n.length;r<i;r++)this.extend(n[r])}function z(t,e){return t instanceof R?t:new R(t,e)}function N(t,e,n){if(isNaN(t)||isNaN(e))throw new Error("Invalid LatLng object: ("+t+", "+e+")");this.lat=+t,this.lng=+e,void 0!==n&&(this.alt=+n)}function F(t,e,n){return t instanceof N?t:v(t)&&"object"!==typeof t[0]?3===t.length?new N(t[0],t[1],t[2]):2===t.length?new N(t[0],t[1]):null:void 0===t||null===t?t:"object"===typeof t&&"lat"in t?new N(t.lat,"lng"in t?t.lng:t.lon,t.alt):void 0===e?null:new N(t,e,n)}P.prototype={clone:function(){return new P(this.x,this.y)},add:function(t){return this.clone()._add(j(t))},_add:function(t){return this.x+=t.x,this.y+=t.y,this},subtract:function(t){return this.clone()._subtract(j(t))},_subtract:function(t){return this.x-=t.x,this.y-=t.y,this},divideBy:function(t){return this.clone()._divideBy(t)},_divideBy:function(t){return this.x/=t,this.y/=t,this},multiplyBy:function(t){return this.clone()._multiplyBy(t)},_multiplyBy:function(t){return this.x*=t,this.y*=t,this},scaleBy:function(t){return new P(this.x*t.x,this.y*t.y)},unscaleBy:function(t){return new P(this.x/t.x,this.y/t.y)},round:function(){return this.clone()._round()},_round:function(){return this.x=Math.round(this.x),this.y=Math.round(this.y),this},floor:function(){return this.clone()._floor()},_floor:function(){return this.x=Math.floor(this.x),this.y=Math.floor(this.y),this},ceil:function(){return this.clone()._ceil()},_ceil:function(){return this.x=Math.ceil(this.x),this.y=Math.ceil(this.y),this},trunc:function(){return this.clone()._trunc()},_trunc:function(){return this.x=E(this.x),this.y=E(this.y),this},distanceTo:function(t){t=j(t);var e=t.x-this.x,n=t.y-this.y;return Math.sqrt(e*e+n*n)},equals:function(t){return t=j(t),t.x===this.x&&t.y===this.y},contains:function(t){return t=j(t),Math.abs(t.x)<=Math.abs(this.x)&&Math.abs(t.y)<=Math.abs(this.y)},toString:function(){return"Point("+c(this.x)+", "+c(this.y)+")"}},H.prototype={extend:function(t){return t=j(t),this.min||this.max?(this.min.x=Math.min(t.x,this.min.x),this.max.x=Math.max(t.x,this.max.x),this.min.y=Math.min(t.y,this.min.y),this.max.y=Math.max(t.y,this.max.y)):(this.min=t.clone(),this.max=t.clone()),this},getCenter:function(t){return new P((this.min.x+this.max.x)/2,(this.min.y+this.max.y)/2,t)},getBottomLeft:function(){return new P(this.min.x,this.max.y)},getTopRight:function(){return new P(this.max.x,this.min.y)},getTopLeft:function(){return this.min},getBottomRight:function(){return this.max},getSize:function(){return this.max.subtract(this.min)},contains:function(t){var e,n;return t="number"===typeof t[0]||t instanceof P?j(t):I(t),t instanceof H?(e=t.min,n=t.max):e=n=t,e.x>=this.min.x&&n.x<=this.max.x&&e.y>=this.min.y&&n.y<=this.max.y},intersects:function(t){t=I(t);var e=this.min,n=this.max,r=t.min,i=t.max,a=i.x>=e.x&&r.x<=n.x,o=i.y>=e.y&&r.y<=n.y;return a&&o},overlaps:function(t){t=I(t);var e=this.min,n=this.max,r=t.min,i=t.max,a=i.x>e.x&&r.x<n.x,o=i.y>e.y&&r.y<n.y;return a&&o},isValid:function(){return!(!this.min||!this.max)}},R.prototype={extend:function(t){var e,n,r=this._southWest,i=this._northEast;if(t instanceof N)e=t,n=t;else{if(!(t instanceof R))return t?this.extend(F(t)||z(t)):this;if(e=t._southWest,n=t._northEast,!e||!n)return this}return r||i?(r.lat=Math.min(e.lat,r.lat),r.lng=Math.min(e.lng,r.lng),i.lat=Math.max(n.lat,i.lat),i.lng=Math.max(n.lng,i.lng)):(this._southWest=new N(e.lat,e.lng),this._northEast=new N(n.lat,n.lng)),this},pad:function(t){var e=this._southWest,n=this._northEast,r=Math.abs(e.lat-n.lat)*t,i=Math.abs(e.lng-n.lng)*t;return new R(new N(e.lat-r,e.lng-i),new N(n.lat+r,n.lng+i))},getCenter:function(){return new N((this._southWest.lat+this._northEast.lat)/2,(this._southWest.lng+this._northEast.lng)/2)},getSouthWest:function(){return this._southWest},getNorthEast:function(){return this._northEast},getNorthWest:function(){return new N(this.getNorth(),this.getWest())},getSouthEast:function(){return new N(this.getSouth(),this.getEast())},getWest:function(){return this._southWest.lng},getSouth:function(){return this._southWest.lat},getEast:function(){return this._northEast.lng},getNorth:function(){return this._northEast.lat},contains:function(t){t="number"===typeof t[0]||t instanceof N||"lat"in t?F(t):z(t);var e,n,r=this._southWest,i=this._northEast;return t instanceof R?(e=t.getSouthWest(),n=t.getNorthEast()):e=n=t,e.lat>=r.lat&&n.lat<=i.lat&&e.lng>=r.lng&&n.lng<=i.lng},intersects:function(t){t=z(t);var e=this._southWest,n=this._northEast,r=t.getSouthWest(),i=t.getNorthEast(),a=i.lat>=e.lat&&r.lat<=n.lat,o=i.lng>=e.lng&&r.lng<=n.lng;return a&&o},overlaps:function(t){t=z(t);var e=this._southWest,n=this._northEast,r=t.getSouthWest(),i=t.getNorthEast(),a=i.lat>e.lat&&r.lat<n.lat,o=i.lng>e.lng&&r.lng<n.lng;return a&&o},toBBoxString:function(){return[this.getWest(),this.getSouth(),this.getEast(),this.getNorth()].join(",")},equals:function(t,e){return!!t&&(t=z(t),this._southWest.equals(t.getSouthWest(),e)&&this._northEast.equals(t.getNorthEast(),e))},isValid:function(){return!(!this._southWest||!this._northEast)}},N.prototype={equals:function(t,e){if(!t)return!1;t=F(t);var n=Math.max(Math.abs(this.lat-t.lat),Math.abs(this.lng-t.lng));return n<=(void 0===e?1e-9:e)},toString:function(t){return"LatLng("+c(this.lat,t)+", "+c(this.lng,t)+")"},distanceTo:function(t){return W.distance(this,F(t))},wrap:function(){return W.wrapLatLng(this)},toBounds:function(t){var e=180*t/40075017,n=e/Math.cos(Math.PI/180*this.lat);return z([this.lat-e,this.lng-n],[this.lat+e,this.lng+n])},clone:function(){return new N(this.lat,this.lng,this.alt)}};var B={latLngToPoint:function(t,e){var n=this.projection.project(t),r=this.scale(e);return this.transformation._transform(n,r)},pointToLatLng:function(t,e){var n=this.scale(e),r=this.transformation.untransform(t,n);return this.projection.unproject(r)},project:function(t){return this.projection.project(t)},unproject:function(t){return this.projection.unproject(t)},scale:function(t){return 256*Math.pow(2,t)},zoom:function(t){return Math.log(t/256)/Math.LN2},getProjectedBounds:function(t){if(this.infinite)return null;var e=this.projection.bounds,n=this.scale(t),r=this.transformation.transform(e.min,n),i=this.transformation.transform(e.max,n);return new H(r,i)},infinite:!1,wrapLatLng:function(t){var e=this.wrapLng?u(t.lng,this.wrapLng,!0):t.lng,n=this.wrapLat?u(t.lat,this.wrapLat,!0):t.lat,r=t.alt;return new N(n,e,r)},wrapLatLngBounds:function(t){var e=t.getCenter(),n=this.wrapLatLng(e),r=e.lat-n.lat,i=e.lng-n.lng;if(0===r&&0===i)return t;var a=t.getSouthWest(),o=t.getNorthEast(),s=new N(a.lat-r,a.lng-i),u=new N(o.lat-r,o.lng-i);return new R(s,u)}},W=n({},B,{wrapLng:[-180,180],R:6371e3,distance:function(t,e){var n=Math.PI/180,r=t.lat*n,i=e.lat*n,a=Math.sin((e.lat-t.lat)*n/2),o=Math.sin((e.lng-t.lng)*n/2),s=a*a+Math.cos(r)*Math.cos(i)*o*o,u=2*Math.atan2(Math.sqrt(s),Math.sqrt(1-s));return this.R*u}}),$=6378137,U={R:$,MAX_LATITUDE:85.0511287798,project:function(t){var e=Math.PI/180,n=this.MAX_LATITUDE,r=Math.max(Math.min(n,t.lat),-n),i=Math.sin(r*e);return new P(this.R*t.lng*e,this.R*Math.log((1+i)/(1-i))/2)},unproject:function(t){var e=180/Math.PI;return new N((2*Math.atan(Math.exp(t.y/this.R))-Math.PI/2)*e,t.x*e/this.R)},bounds:function(){var t=$*Math.PI;return new H([-t,-t],[t,t])}()};function V(t,e,n,r){if(v(t))return this._a=t[0],this._b=t[1],this._c=t[2],void(this._d=t[3]);this._a=t,this._b=e,this._c=n,this._d=r}function Z(t,e,n,r){return new V(t,e,n,r)}V.prototype={transform:function(t,e){return this._transform(t.clone(),e)},_transform:function(t,e){return e=e||1,t.x=e*(this._a*t.x+this._b),t.y=e*(this._c*t.y+this._d),t},untransform:function(t,e){return e=e||1,new P((t.x/e-this._b)/this._a,(t.y/e-this._d)/this._c)}};var q=n({},W,{code:"EPSG:3857",projection:U,transformation:function(){var t=.5/(Math.PI*U.R);return Z(t,.5,-t,.5)}()}),G=n({},q,{code:"EPSG:900913"});function J(t){return document.createElementNS("http://www.w3.org/2000/svg",t)}function K(t,e){var n,r,i,a,o,s,u="";for(n=0,i=t.length;n<i;n++){for(o=t[n],r=0,a=o.length;r<a;r++)s=o[r],u+=(r?"L":"M")+s.x+" "+s.y;u+=e?Yt?"z":"x":""}return u||"M0 0"}var X=document.documentElement.style,Q="ActiveXObject"in window,tt=Q&&!document.addEventListener,et="msLaunchUri"in navigator&&!("documentMode"in document),nt=At("webkit"),rt=At("android"),it=At("android 2")||At("android 3"),at=parseInt(/WebKit\/([0-9]+)|$/.exec(navigator.userAgent)[1],10),ot=rt&&At("Google")&&at<537&&!("AudioNode"in window),st=!!window.opera,ut=!et&&At("chrome"),lt=At("gecko")&&!nt&&!st&&!Q,ct=!ut&&At("safari"),dt=At("phantom"),ht="OTransition"in X,ft=0===navigator.platform.indexOf("Win"),pt=Q&&"transition"in X,mt="WebKitCSSMatrix"in window&&"m11"in new window.WebKitCSSMatrix&&!it,_t="MozPerspective"in X,vt=!window.L_DISABLE_3D&&(pt||mt||_t)&&!ht&&!dt,gt="undefined"!==typeof orientation||At("mobile"),yt=gt&&nt,bt=gt&&mt,wt=!window.PointerEvent&&window.MSPointerEvent,Mt=!(!window.PointerEvent&&!wt),xt=!window.L_NO_TOUCH&&(Mt||"ontouchstart"in window||window.DocumentTouch&&document instanceof window.DocumentTouch),Lt=gt&&st,kt=gt&&lt,Tt=(window.devicePixelRatio||window.screen.deviceXDPI/window.screen.logicalXDPI)>1,St=function(){var t=!1;try{var e=Object.defineProperty({},"passive",{get:function(){t=!0}});window.addEventListener("testPassiveEventSupport",l,e),window.removeEventListener("testPassiveEventSupport",l,e)}catch(n){}return t}(),Dt=function(){return!!document.createElement("canvas").getContext}(),Yt=!(!document.createElementNS||!J("svg").createSVGRect),Ot=!Yt&&function(){try{var t=document.createElement("div");t.innerHTML='<v:shape adj="1"/>';var e=t.firstChild;return e.style.behavior="url(#default#VML)",e&&"object"===typeof e.adj}catch(n){return!1}}();function At(t){return navigator.userAgent.toLowerCase().indexOf(t)>=0}var Ct={ie:Q,ielt9:tt,edge:et,webkit:nt,android:rt,android23:it,androidStock:ot,opera:st,chrome:ut,gecko:lt,safari:ct,phantom:dt,opera12:ht,win:ft,ie3d:pt,webkit3d:mt,gecko3d:_t,any3d:vt,mobile:gt,mobileWebkit:yt,mobileWebkit3d:bt,msPointer:wt,pointer:Mt,touch:xt,mobileOpera:Lt,mobileGecko:kt,retina:Tt,passiveEvents:St,canvas:Dt,svg:Yt,vml:Ot},Pt=wt?"MSPointerDown":"pointerdown",Et=wt?"MSPointerMove":"pointermove",jt=wt?"MSPointerUp":"pointerup",Ht=wt?"MSPointerCancel":"pointercancel",It={},Rt=!1;function zt(t,e,n,r){return"touchstart"===e?Ft(t,n,r):"touchmove"===e?Vt(t,n,r):"touchend"===e&&Zt(t,n,r),this}function Nt(t,e,n){var r=t["_leaflet_"+e+n];return"touchstart"===e?t.removeEventListener(Pt,r,!1):"touchmove"===e?t.removeEventListener(Et,r,!1):"touchend"===e&&(t.removeEventListener(jt,r,!1),t.removeEventListener(Ht,r,!1)),this}function Ft(t,e,n){var r=i((function(t){t.MSPOINTER_TYPE_TOUCH&&t.pointerType===t.MSPOINTER_TYPE_TOUCH&&We(t),Ut(t,e)}));t["_leaflet_touchstart"+n]=r,t.addEventListener(Pt,r,!1),Rt||(document.addEventListener(Pt,Bt,!0),document.addEventListener(Et,Wt,!0),document.addEventListener(jt,$t,!0),document.addEventListener(Ht,$t,!0),Rt=!0)}function Bt(t){It[t.pointerId]=t}function Wt(t){It[t.pointerId]&&(It[t.pointerId]=t)}function $t(t){delete It[t.pointerId]}function Ut(t,e){for(var n in t.touches=[],It)t.touches.push(It[n]);t.changedTouches=[t],e(t)}function Vt(t,e,n){var r=function(t){t.pointerType===(t.MSPOINTER_TYPE_MOUSE||"mouse")&&0===t.buttons||Ut(t,e)};t["_leaflet_touchmove"+n]=r,t.addEventListener(Et,r,!1)}function Zt(t,e,n){var r=function(t){Ut(t,e)};t["_leaflet_touchend"+n]=r,t.addEventListener(jt,r,!1),t.addEventListener(Ht,r,!1)}var qt=wt?"MSPointerDown":Mt?"pointerdown":"touchstart",Gt=wt?"MSPointerUp":Mt?"pointerup":"touchend",Jt="_leaflet_";function Kt(t,e,n){var r,i,a=!1,o=250;function s(t){if(Mt){if(!t.isPrimary)return;if("mouse"===t.pointerType)return}else if(t.touches.length>1)return;var e=Date.now(),n=e-(r||e);i=t.touches?t.touches[0]:t,a=n>0&&n<=o,r=e}function u(t){if(a&&!i.cancelBubble){if(Mt){if("mouse"===t.pointerType)return;var n,o,s={};for(o in i)n=i[o],s[o]=n&&n.bind?n.bind(i):n;i=s}i.type="dblclick",i.button=0,e(i),r=null}}return t[Jt+qt+n]=s,t[Jt+Gt+n]=u,t[Jt+"dblclick"+n]=e,t.addEventListener(qt,s,!!St&&{passive:!1}),t.addEventListener(Gt,u,!!St&&{passive:!1}),t.addEventListener("dblclick",e,!1),this}function Xt(t,e){var n=t[Jt+qt+e],r=t[Jt+Gt+e],i=t[Jt+"dblclick"+e];return t.removeEventListener(qt,n,!!St&&{passive:!1}),t.removeEventListener(Gt,r,!!St&&{passive:!1}),t.removeEventListener("dblclick",i,!1),this}var Qt,te,ee,ne,re,ie=we(["transform","webkitTransform","OTransform","MozTransform","msTransform"]),ae=we(["webkitTransition","transition","OTransition","MozTransition","msTransition"]),oe="webkitTransition"===ae||"OTransition"===ae?ae+"End":"transitionend";function se(t){return"string"===typeof t?document.getElementById(t):t}function ue(t,e){var n=t.style[e]||t.currentStyle&&t.currentStyle[e];if((!n||"auto"===n)&&document.defaultView){var r=document.defaultView.getComputedStyle(t,null);n=r?r[e]:null}return"auto"===n?null:n}function le(t,e,n){var r=document.createElement(t);return r.className=e||"",n&&n.appendChild(r),r}function ce(t){var e=t.parentNode;e&&e.removeChild(t)}function de(t){while(t.firstChild)t.removeChild(t.firstChild)}function he(t){var e=t.parentNode;e&&e.lastChild!==t&&e.appendChild(t)}function fe(t){var e=t.parentNode;e&&e.firstChild!==t&&e.insertBefore(t,e.firstChild)}function pe(t,e){if(void 0!==t.classList)return t.classList.contains(e);var n=ge(t);return n.length>0&&new RegExp("(^|\\s)"+e+"(\\s|$)").test(n)}function me(t,e){if(void 0!==t.classList)for(var n=h(e),r=0,i=n.length;r<i;r++)t.classList.add(n[r]);else if(!pe(t,e)){var a=ge(t);ve(t,(a?a+" ":"")+e)}}function _e(t,e){void 0!==t.classList?t.classList.remove(e):ve(t,d((" "+ge(t)+" ").replace(" "+e+" "," ")))}function ve(t,e){void 0===t.className.baseVal?t.className=e:t.className.baseVal=e}function ge(t){return t.correspondingElement&&(t=t.correspondingElement),void 0===t.className.baseVal?t.className:t.className.baseVal}function ye(t,e){"opacity"in t.style?t.style.opacity=e:"filter"in t.style&&be(t,e)}function be(t,e){var n=!1,r="DXImageTransform.Microsoft.Alpha";try{n=t.filters.item(r)}catch(i){if(1===e)return}e=Math.round(100*e),n?(n.Enabled=100!==e,n.Opacity=e):t.style.filter+=" progid:"+r+"(opacity="+e+")"}function we(t){for(var e=document.documentElement.style,n=0;n<t.length;n++)if(t[n]in e)return t[n];return!1}function Me(t,e,n){var r=e||new P(0,0);t.style[ie]=(pt?"translate("+r.x+"px,"+r.y+"px)":"translate3d("+r.x+"px,"+r.y+"px,0)")+(n?" scale("+n+")":"")}function xe(t,e){t._leaflet_pos=e,vt?Me(t,e):(t.style.left=e.x+"px",t.style.top=e.y+"px")}function Le(t){return t._leaflet_pos||new P(0,0)}if("onselectstart"in document)Qt=function(){Pe(window,"selectstart",We)},te=function(){je(window,"selectstart",We)};else{var ke=we(["userSelect","WebkitUserSelect","OUserSelect","MozUserSelect","msUserSelect"]);Qt=function(){if(ke){var t=document.documentElement.style;ee=t[ke],t[ke]="none"}},te=function(){ke&&(document.documentElement.style[ke]=ee,ee=void 0)}}function Te(){Pe(window,"dragstart",We)}function Se(){je(window,"dragstart",We)}function De(t){while(-1===t.tabIndex)t=t.parentNode;t.style&&(Ye(),ne=t,re=t.style.outline,t.style.outline="none",Pe(window,"keydown",Ye))}function Ye(){ne&&(ne.style.outline=re,ne=void 0,re=void 0,je(window,"keydown",Ye))}function Oe(t){do{t=t.parentNode}while((!t.offsetWidth||!t.offsetHeight)&&t!==document.body);return t}function Ae(t){var e=t.getBoundingClientRect();return{x:e.width/t.offsetWidth||1,y:e.height/t.offsetHeight||1,boundingClientRect:e}}var Ce={TRANSFORM:ie,TRANSITION:ae,TRANSITION_END:oe,get:se,getStyle:ue,create:le,remove:ce,empty:de,toFront:he,toBack:fe,hasClass:pe,addClass:me,removeClass:_e,setClass:ve,getClass:ge,setOpacity:ye,testProp:we,setTransform:Me,setPosition:xe,getPosition:Le,disableTextSelection:Qt,enableTextSelection:te,disableImageDrag:Te,enableImageDrag:Se,preventOutline:De,restoreOutline:Ye,getSizedParentNode:Oe,getScale:Ae};function Pe(t,e,n,r){if("object"===typeof e)for(var i in e)Re(t,i,e[i],n);else{e=h(e);for(var a=0,o=e.length;a<o;a++)Re(t,e[a],n,r)}return this}var Ee="_leaflet_events";function je(t,e,n,r){if("object"===typeof e)for(var i in e)ze(t,i,e[i],n);else if(e){e=h(e);for(var a=0,o=e.length;a<o;a++)ze(t,e[a],n,r)}else{for(var s in t[Ee])ze(t,s,t[Ee][s]);delete t[Ee]}return this}function He(){if(Mt)return!(et||ct)}var Ie={mouseenter:"mouseover",mouseleave:"mouseout",wheel:!("onwheel"in window)&&"mousewheel"};function Re(t,e,n,r){var i=e+o(n)+(r?"_"+o(r):"");if(t[Ee]&&t[Ee][i])return this;var a=function(e){return n.call(r||t,e||window.event)},s=a;Mt&&0===e.indexOf("touch")?zt(t,e,a,i):xt&&"dblclick"===e&&!He()?Kt(t,a,i):"addEventListener"in t?"touchstart"===e||"touchmove"===e||"wheel"===e||"mousewheel"===e?t.addEventListener(Ie[e]||e,a,!!St&&{passive:!1}):"mouseenter"===e||"mouseleave"===e?(a=function(e){e=e||window.event,Ke(t,e)&&s(e)},t.addEventListener(Ie[e],a,!1)):t.addEventListener(e,s,!1):"attachEvent"in t&&t.attachEvent("on"+e,a),t[Ee]=t[Ee]||{},t[Ee][i]=a}function ze(t,e,n,r){var i=e+o(n)+(r?"_"+o(r):""),a=t[Ee]&&t[Ee][i];if(!a)return this;Mt&&0===e.indexOf("touch")?Nt(t,e,i):xt&&"dblclick"===e&&!He()?Xt(t,i):"removeEventListener"in t?t.removeEventListener(Ie[e]||e,a,!1):"detachEvent"in t&&t.detachEvent("on"+e,a),t[Ee][i]=null}function Ne(t){return t.stopPropagation?t.stopPropagation():t.originalEvent?t.originalEvent._stopped=!0:t.cancelBubble=!0,Je(t),this}function Fe(t){return Re(t,"wheel",Ne),this}function Be(t){return Pe(t,"mousedown touchstart dblclick",Ne),Re(t,"click",Ge),this}function We(t){return t.preventDefault?t.preventDefault():t.returnValue=!1,this}function $e(t){return We(t),Ne(t),this}function Ue(t,e){if(!e)return new P(t.clientX,t.clientY);var n=Ae(e),r=n.boundingClientRect;return new P((t.clientX-r.left)/n.x-e.clientLeft,(t.clientY-r.top)/n.y-e.clientTop)}var Ve=ft&&ut?2*window.devicePixelRatio:lt?window.devicePixelRatio:1;function Ze(t){return et?t.wheelDeltaY/2:t.deltaY&&0===t.deltaMode?-t.deltaY/Ve:t.deltaY&&1===t.deltaMode?20*-t.deltaY:t.deltaY&&2===t.deltaMode?60*-t.deltaY:t.deltaX||t.deltaZ?0:t.wheelDelta?(t.wheelDeltaY||t.wheelDelta)/2:t.detail&&Math.abs(t.detail)<32765?20*-t.detail:t.detail?t.detail/-32765*60:0}var qe={};function Ge(t){qe[t.type]=!0}function Je(t){var e=qe[t.type];return qe[t.type]=!1,e}function Ke(t,e){var n=e.relatedTarget;if(!n)return!0;try{while(n&&n!==t)n=n.parentNode}catch(r){return!1}return n!==t}var Xe={on:Pe,off:je,stopPropagation:Ne,disableScrollPropagation:Fe,disableClickPropagation:Be,preventDefault:We,stop:$e,getMousePosition:Ue,getWheelDelta:Ze,fakeStop:Ge,skipped:Je,isExternalTarget:Ke,addListener:Pe,removeListener:je},Qe=C.extend({run:function(t,e,n,r){this.stop(),this._el=t,this._inProgress=!0,this._duration=n||.25,this._easeOutPower=1/Math.max(r||.5,.2),this._startPos=Le(t),this._offset=e.subtract(this._startPos),this._startTime=+new Date,this.fire("start"),this._animate()},stop:function(){this._inProgress&&(this._step(!0),this._complete())},_animate:function(){this._animId=T(this._animate,this),this._step()},_step:function(t){var e=+new Date-this._startTime,n=1e3*this._duration;e<n?this._runFrame(this._easeOut(e/n),t):(this._runFrame(1),this._complete())},_runFrame:function(t,e){var n=this._startPos.add(this._offset.multiplyBy(t));e&&n._round(),xe(this._el,n),this.fire("step")},_complete:function(){S(this._animId),this._inProgress=!1,this.fire("end")},_easeOut:function(t){return 1-Math.pow(1-t,this._easeOutPower)}}),tn=C.extend({options:{crs:q,center:void 0,zoom:void 0,minZoom:void 0,maxZoom:void 0,layers:[],maxBounds:void 0,renderer:void 0,zoomAnimation:!0,zoomAnimationThreshold:4,fadeAnimation:!0,markerZoomAnimation:!0,transform3DLimit:8388608,zoomSnap:1,zoomDelta:1,trackResize:!0},initialize:function(t,e){e=f(this,e),this._handlers=[],this._layers={},this._zoomBoundLayers={},this._sizeChanged=!0,this._initContainer(t),this._initLayout(),this._onResize=i(this._onResize,this),this._initEvents(),e.maxBounds&&this.setMaxBounds(e.maxBounds),void 0!==e.zoom&&(this._zoom=this._limitZoom(e.zoom)),e.center&&void 0!==e.zoom&&this.setView(F(e.center),e.zoom,{reset:!0}),this.callInitHooks(),this._zoomAnimated=ae&&vt&&!Lt&&this.options.zoomAnimation,this._zoomAnimated&&(this._createAnimProxy(),Pe(this._proxy,oe,this._catchTransitionEnd,this)),this._addLayers(this.options.layers)},setView:function(t,e,r){if(e=void 0===e?this._zoom:this._limitZoom(e),t=this._limitCenter(F(t),e,this.options.maxBounds),r=r||{},this._stop(),this._loaded&&!r.reset&&!0!==r){void 0!==r.animate&&(r.zoom=n({animate:r.animate},r.zoom),r.pan=n({animate:r.animate,duration:r.duration},r.pan));var i=this._zoom!==e?this._tryAnimatedZoom&&this._tryAnimatedZoom(t,e,r.zoom):this._tryAnimatedPan(t,r.pan);if(i)return clearTimeout(this._sizeTimer),this}return this._resetView(t,e),this},setZoom:function(t,e){return this._loaded?this.setView(this.getCenter(),t,{zoom:e}):(this._zoom=t,this)},zoomIn:function(t,e){return t=t||(vt?this.options.zoomDelta:1),this.setZoom(this._zoom+t,e)},zoomOut:function(t,e){return t=t||(vt?this.options.zoomDelta:1),this.setZoom(this._zoom-t,e)},setZoomAround:function(t,e,n){var r=this.getZoomScale(e),i=this.getSize().divideBy(2),a=t instanceof P?t:this.latLngToContainerPoint(t),o=a.subtract(i).multiplyBy(1-1/r),s=this.containerPointToLatLng(i.add(o));return this.setView(s,e,{zoom:n})},_getBoundsCenterZoom:function(t,e){e=e||{},t=t.getBounds?t.getBounds():z(t);var n=j(e.paddingTopLeft||e.padding||[0,0]),r=j(e.paddingBottomRight||e.padding||[0,0]),i=this.getBoundsZoom(t,!1,n.add(r));if(i="number"===typeof e.maxZoom?Math.min(e.maxZoom,i):i,i===1/0)return{center:t.getCenter(),zoom:i};var a=r.subtract(n).divideBy(2),o=this.project(t.getSouthWest(),i),s=this.project(t.getNorthEast(),i),u=this.unproject(o.add(s).divideBy(2).add(a),i);return{center:u,zoom:i}},fitBounds:function(t,e){if(t=z(t),!t.isValid())throw new Error("Bounds are not valid.");var n=this._getBoundsCenterZoom(t,e);return this.setView(n.center,n.zoom,e)},fitWorld:function(t){return this.fitBounds([[-90,-180],[90,180]],t)},panTo:function(t,e){return this.setView(t,this._zoom,{pan:e})},panBy:function(t,e){if(t=j(t).round(),e=e||{},!t.x&&!t.y)return this.fire("moveend");if(!0!==e.animate&&!this.getSize().contains(t))return this._resetView(this.unproject(this.project(this.getCenter()).add(t)),this.getZoom()),this;if(this._panAnim||(this._panAnim=new Qe,this._panAnim.on({step:this._onPanTransitionStep,end:this._onPanTransitionEnd},this)),e.noMoveStart||this.fire("movestart"),!1!==e.animate){me(this._mapPane,"leaflet-pan-anim");var n=this._getMapPanePos().subtract(t).round();this._panAnim.run(this._mapPane,n,e.duration||.25,e.easeLinearity)}else this._rawPanBy(t),this.fire("move").fire("moveend");return this},flyTo:function(t,e,n){if(n=n||{},!1===n.animate||!vt)return this.setView(t,e,n);this._stop();var r=this.project(this.getCenter()),i=this.project(t),a=this.getSize(),o=this._zoom;t=F(t),e=void 0===e?o:e;var s=Math.max(a.x,a.y),u=s*this.getZoomScale(o,e),l=i.distanceTo(r)||1,c=1.42,d=c*c;function h(t){var e=t?-1:1,n=t?u:s,r=u*u-s*s+e*d*d*l*l,i=2*n*d*l,a=r/i,o=Math.sqrt(a*a+1)-a,c=o<1e-9?-18:Math.log(o);return c}function f(t){return(Math.exp(t)-Math.exp(-t))/2}function p(t){return(Math.exp(t)+Math.exp(-t))/2}function m(t){return f(t)/p(t)}var _=h(0);function v(t){return s*(p(_)/p(_+c*t))}function g(t){return s*(p(_)*m(_+c*t)-f(_))/d}function y(t){return 1-Math.pow(1-t,1.5)}var b=Date.now(),w=(h(1)-_)/c,M=n.duration?1e3*n.duration:1e3*w*.8;function x(){var n=(Date.now()-b)/M,a=y(n)*w;n<=1?(this._flyToFrame=T(x,this),this._move(this.unproject(r.add(i.subtract(r).multiplyBy(g(a)/l)),o),this.getScaleZoom(s/v(a),o),{flyTo:!0})):this._move(t,e)._moveEnd(!0)}return this._moveStart(!0,n.noMoveStart),x.call(this),this},flyToBounds:function(t,e){var n=this._getBoundsCenterZoom(t,e);return this.flyTo(n.center,n.zoom,e)},setMaxBounds:function(t){return t=z(t),t.isValid()?(this.options.maxBounds&&this.off("moveend",this._panInsideMaxBounds),this.options.maxBounds=t,this._loaded&&this._panInsideMaxBounds(),this.on("moveend",this._panInsideMaxBounds)):(this.options.maxBounds=null,this.off("moveend",this._panInsideMaxBounds))},setMinZoom:function(t){var e=this.options.minZoom;return this.options.minZoom=t,this._loaded&&e!==t&&(this.fire("zoomlevelschange"),this.getZoom()<this.options.minZoom)?this.setZoom(t):this},setMaxZoom:function(t){var e=this.options.maxZoom;return this.options.maxZoom=t,this._loaded&&e!==t&&(this.fire("zoomlevelschange"),this.getZoom()>this.options.maxZoom)?this.setZoom(t):this},panInsideBounds:function(t,e){this._enforcingBounds=!0;var n=this.getCenter(),r=this._limitCenter(n,this._zoom,z(t));return n.equals(r)||this.panTo(r,e),this._enforcingBounds=!1,this},panInside:function(t,e){e=e||{};var n=j(e.paddingTopLeft||e.padding||[0,0]),r=j(e.paddingBottomRight||e.padding||[0,0]),i=this.getCenter(),a=this.project(i),o=this.project(t),s=this.getPixelBounds(),u=s.getSize().divideBy(2),l=I([s.min.add(n),s.max.subtract(r)]);if(!l.contains(o)){this._enforcingBounds=!0;var c=a.subtract(o),d=j(o.x+c.x,o.y+c.y);(o.x<l.min.x||o.x>l.max.x)&&(d.x=a.x-c.x,c.x>0?d.x+=u.x-n.x:d.x-=u.x-r.x),(o.y<l.min.y||o.y>l.max.y)&&(d.y=a.y-c.y,c.y>0?d.y+=u.y-n.y:d.y-=u.y-r.y),this.panTo(this.unproject(d),e),this._enforcingBounds=!1}return this},invalidateSize:function(t){if(!this._loaded)return this;t=n({animate:!1,pan:!0},!0===t?{animate:!0}:t);var e=this.getSize();this._sizeChanged=!0,this._lastCenter=null;var r=this.getSize(),a=e.divideBy(2).round(),o=r.divideBy(2).round(),s=a.subtract(o);return s.x||s.y?(t.animate&&t.pan?this.panBy(s):(t.pan&&this._rawPanBy(s),this.fire("move"),t.debounceMoveend?(clearTimeout(this._sizeTimer),this._sizeTimer=setTimeout(i(this.fire,this,"moveend"),200)):this.fire("moveend")),this.fire("resize",{oldSize:e,newSize:r})):this},stop:function(){return this.setZoom(this._limitZoom(this._zoom)),this.options.zoomSnap||this.fire("viewreset"),this._stop()},locate:function(t){if(t=this._locateOptions=n({timeout:1e4,watch:!1},t),!("geolocation"in navigator))return this._handleGeolocationError({code:0,message:"Geolocation not supported."}),this;var e=i(this._handleGeolocationResponse,this),r=i(this._handleGeolocationError,this);return t.watch?this._locationWatchId=navigator.geolocation.watchPosition(e,r,t):navigator.geolocation.getCurrentPosition(e,r,t),this},stopLocate:function(){return navigator.geolocation&&navigator.geolocation.clearWatch&&navigator.geolocation.clearWatch(this._locationWatchId),this._locateOptions&&(this._locateOptions.setView=!1),this},_handleGeolocationError:function(t){var e=t.code,n=t.message||(1===e?"permission denied":2===e?"position unavailable":"timeout");this._locateOptions.setView&&!this._loaded&&this.fitWorld(),this.fire("locationerror",{code:e,message:"Geolocation error: "+n+"."})},_handleGeolocationResponse:function(t){var e=t.coords.latitude,n=t.coords.longitude,r=new N(e,n),i=r.toBounds(2*t.coords.accuracy),a=this._locateOptions;if(a.setView){var o=this.getBoundsZoom(i);this.setView(r,a.maxZoom?Math.min(o,a.maxZoom):o)}var s={latlng:r,bounds:i,timestamp:t.timestamp};for(var u in t.coords)"number"===typeof t.coords[u]&&(s[u]=t.coords[u]);this.fire("locationfound",s)},addHandler:function(t,e){if(!e)return this;var n=this[t]=new e(this);return this._handlers.push(n),this.options[t]&&n.enable(),this},remove:function(){if(this._initEvents(!0),this.off("moveend",this._panInsideMaxBounds),this._containerId!==this._container._leaflet_id)throw new Error("Map container is being reused by another instance");try{delete this._container._leaflet_id,delete this._containerId}catch(e){this._container._leaflet_id=void 0,this._containerId=void 0}var t;for(t in void 0!==this._locationWatchId&&this.stopLocate(),this._stop(),ce(this._mapPane),this._clearControlPos&&this._clearControlPos(),this._resizeRequest&&(S(this._resizeRequest),this._resizeRequest=null),this._clearHandlers(),this._loaded&&this.fire("unload"),this._layers)this._layers[t].remove();for(t in this._panes)ce(this._panes[t]);return this._layers=[],this._panes=[],delete this._mapPane,delete this._renderer,this},createPane:function(t,e){var n="leaflet-pane"+(t?" leaflet-"+t.replace("Pane","")+"-pane":""),r=le("div",n,e||this._mapPane);return t&&(this._panes[t]=r),r},getCenter:function(){return this._checkIfLoaded(),this._lastCenter&&!this._moved()?this._lastCenter:this.layerPointToLatLng(this._getCenterLayerPoint())},getZoom:function(){return this._zoom},getBounds:function(){var t=this.getPixelBounds(),e=this.unproject(t.getBottomLeft()),n=this.unproject(t.getTopRight());return new R(e,n)},getMinZoom:function(){return void 0===this.options.minZoom?this._layersMinZoom||0:this.options.minZoom},getMaxZoom:function(){return void 0===this.options.maxZoom?void 0===this._layersMaxZoom?1/0:this._layersMaxZoom:this.options.maxZoom},getBoundsZoom:function(t,e,n){t=z(t),n=j(n||[0,0]);var r=this.getZoom()||0,i=this.getMinZoom(),a=this.getMaxZoom(),o=t.getNorthWest(),s=t.getSouthEast(),u=this.getSize().subtract(n),l=I(this.project(s,r),this.project(o,r)).getSize(),c=vt?this.options.zoomSnap:1,d=u.x/l.x,h=u.y/l.y,f=e?Math.max(d,h):Math.min(d,h);return r=this.getScaleZoom(f,r),c&&(r=Math.round(r/(c/100))*(c/100),r=e?Math.ceil(r/c)*c:Math.floor(r/c)*c),Math.max(i,Math.min(a,r))},getSize:function(){return this._size&&!this._sizeChanged||(this._size=new P(this._container.clientWidth||0,this._container.clientHeight||0),this._sizeChanged=!1),this._size.clone()},getPixelBounds:function(t,e){var n=this._getTopLeftPoint(t,e);return new H(n,n.add(this.getSize()))},getPixelOrigin:function(){return this._checkIfLoaded(),this._pixelOrigin},getPixelWorldBounds:function(t){return this.options.crs.getProjectedBounds(void 0===t?this.getZoom():t)},getPane:function(t){return"string"===typeof t?this._panes[t]:t},getPanes:function(){return this._panes},getContainer:function(){return this._container},getZoomScale:function(t,e){var n=this.options.crs;return e=void 0===e?this._zoom:e,n.scale(t)/n.scale(e)},getScaleZoom:function(t,e){var n=this.options.crs;e=void 0===e?this._zoom:e;var r=n.zoom(t*n.scale(e));return isNaN(r)?1/0:r},project:function(t,e){return e=void 0===e?this._zoom:e,this.options.crs.latLngToPoint(F(t),e)},unproject:function(t,e){return e=void 0===e?this._zoom:e,this.options.crs.pointToLatLng(j(t),e)},layerPointToLatLng:function(t){var e=j(t).add(this.getPixelOrigin());return this.unproject(e)},latLngToLayerPoint:function(t){var e=this.project(F(t))._round();return e._subtract(this.getPixelOrigin())},wrapLatLng:function(t){return this.options.crs.wrapLatLng(F(t))},wrapLatLngBounds:function(t){return this.options.crs.wrapLatLngBounds(z(t))},distance:function(t,e){return this.options.crs.distance(F(t),F(e))},containerPointToLayerPoint:function(t){return j(t).subtract(this._getMapPanePos())},layerPointToContainerPoint:function(t){return j(t).add(this._getMapPanePos())},containerPointToLatLng:function(t){var e=this.containerPointToLayerPoint(j(t));return this.layerPointToLatLng(e)},latLngToContainerPoint:function(t){return this.layerPointToContainerPoint(this.latLngToLayerPoint(F(t)))},mouseEventToContainerPoint:function(t){return Ue(t,this._container)},mouseEventToLayerPoint:function(t){return this.containerPointToLayerPoint(this.mouseEventToContainerPoint(t))},mouseEventToLatLng:function(t){return this.layerPointToLatLng(this.mouseEventToLayerPoint(t))},_initContainer:function(t){var e=this._container=se(t);if(!e)throw new Error("Map container not found.");if(e._leaflet_id)throw new Error("Map container is already initialized.");Pe(e,"scroll",this._onScroll,this),this._containerId=o(e)},_initLayout:function(){var t=this._container;this._fadeAnimated=this.options.fadeAnimation&&vt,me(t,"leaflet-container"+(xt?" leaflet-touch":"")+(Tt?" leaflet-retina":"")+(tt?" leaflet-oldie":"")+(ct?" leaflet-safari":"")+(this._fadeAnimated?" leaflet-fade-anim":""));var e=ue(t,"position");"absolute"!==e&&"relative"!==e&&"fixed"!==e&&(t.style.position="relative"),this._initPanes(),this._initControlPos&&this._initControlPos()},_initPanes:function(){var t=this._panes={};this._paneRenderers={},this._mapPane=this.createPane("mapPane",this._container),xe(this._mapPane,new P(0,0)),this.createPane("tilePane"),this.createPane("shadowPane"),this.createPane("overlayPane"),this.createPane("markerPane"),this.createPane("tooltipPane"),this.createPane("popupPane"),this.options.markerZoomAnimation||(me(t.markerPane,"leaflet-zoom-hide"),me(t.shadowPane,"leaflet-zoom-hide"))},_resetView:function(t,e){xe(this._mapPane,new P(0,0));var n=!this._loaded;this._loaded=!0,e=this._limitZoom(e),this.fire("viewprereset");var r=this._zoom!==e;this._moveStart(r,!1)._move(t,e)._moveEnd(r),this.fire("viewreset"),n&&this.fire("load")},_moveStart:function(t,e){return t&&this.fire("zoomstart"),e||this.fire("movestart"),this},_move:function(t,e,n){void 0===e&&(e=this._zoom);var r=this._zoom!==e;return this._zoom=e,this._lastCenter=t,this._pixelOrigin=this._getNewPixelOrigin(t),(r||n&&n.pinch)&&this.fire("zoom",n),this.fire("move",n)},_moveEnd:function(t){return t&&this.fire("zoomend"),this.fire("moveend")},_stop:function(){return S(this._flyToFrame),this._panAnim&&this._panAnim.stop(),this},_rawPanBy:function(t){xe(this._mapPane,this._getMapPanePos().subtract(t))},_getZoomSpan:function(){return this.getMaxZoom()-this.getMinZoom()},_panInsideMaxBounds:function(){this._enforcingBounds||this.panInsideBounds(this.options.maxBounds)},_checkIfLoaded:function(){if(!this._loaded)throw new Error("Set map center and zoom first.")},_initEvents:function(t){this._targets={},this._targets[o(this._container)]=this;var e=t?je:Pe;e(this._container,"click dblclick mousedown mouseup mouseover mouseout mousemove contextmenu keypress keydown keyup",this._handleDOMEvent,this),this.options.trackResize&&e(window,"resize",this._onResize,this),vt&&this.options.transform3DLimit&&(t?this.off:this.on).call(this,"moveend",this._onMoveEnd)},_onResize:function(){S(this._resizeRequest),this._resizeRequest=T((function(){this.invalidateSize({debounceMoveend:!0})}),this)},_onScroll:function(){this._container.scrollTop=0,this._container.scrollLeft=0},_onMoveEnd:function(){var t=this._getMapPanePos();Math.max(Math.abs(t.x),Math.abs(t.y))>=this.options.transform3DLimit&&this._resetView(this.getCenter(),this.getZoom())},_findEventTargets:function(t,e){var n,r=[],i="mouseout"===e||"mouseover"===e,a=t.target||t.srcElement,s=!1;while(a){if(n=this._targets[o(a)],n&&("click"===e||"preclick"===e)&&!t._simulated&&this._draggableMoved(n)){s=!0;break}if(n&&n.listens(e,!0)){if(i&&!Ke(a,t))break;if(r.push(n),i)break}if(a===this._container)break;a=a.parentNode}return r.length||s||i||!Ke(a,t)||(r=[this]),r},_handleDOMEvent:function(t){if(this._loaded&&!Je(t)){var e=t.type;"mousedown"!==e&&"keypress"!==e&&"keyup"!==e&&"keydown"!==e||De(t.target||t.srcElement),this._fireDOMEvent(t,e)}},_mouseEvents:["click","dblclick","mouseover","mouseout","contextmenu"],_fireDOMEvent:function(t,e,r){if("click"===t.type){var i=n({},t);i.type="preclick",this._fireDOMEvent(i,i.type,r)}if(!t._stopped&&(r=(r||[]).concat(this._findEventTargets(t,e)),r.length)){var a=r[0];"contextmenu"===e&&a.listens(e,!0)&&We(t);var o={originalEvent:t};if("keypress"!==t.type&&"keydown"!==t.type&&"keyup"!==t.type){var s=a.getLatLng&&(!a._radius||a._radius<=10);o.containerPoint=s?this.latLngToContainerPoint(a.getLatLng()):this.mouseEventToContainerPoint(t),o.layerPoint=this.containerPointToLayerPoint(o.containerPoint),o.latlng=s?a.getLatLng():this.layerPointToLatLng(o.layerPoint)}for(var u=0;u<r.length;u++)if(r[u].fire(e,o,!0),o.originalEvent._stopped||!1===r[u].options.bubblingMouseEvents&&-1!==g(this._mouseEvents,e))return}},_draggableMoved:function(t){return t=t.dragging&&t.dragging.enabled()?t:this,t.dragging&&t.dragging.moved()||this.boxZoom&&this.boxZoom.moved()},_clearHandlers:function(){for(var t=0,e=this._handlers.length;t<e;t++)this._handlers[t].disable()},whenReady:function(t,e){return this._loaded?t.call(e||this,{target:this}):this.on("load",t,e),this},_getMapPanePos:function(){return Le(this._mapPane)||new P(0,0)},_moved:function(){var t=this._getMapPanePos();return t&&!t.equals([0,0])},_getTopLeftPoint:function(t,e){var n=t&&void 0!==e?this._getNewPixelOrigin(t,e):this.getPixelOrigin();return n.subtract(this._getMapPanePos())},_getNewPixelOrigin:function(t,e){var n=this.getSize()._divideBy(2);return this.project(t,e)._subtract(n)._add(this._getMapPanePos())._round()},_latLngToNewLayerPoint:function(t,e,n){var r=this._getNewPixelOrigin(n,e);return this.project(t,e)._subtract(r)},_latLngBoundsToNewLayerBounds:function(t,e,n){var r=this._getNewPixelOrigin(n,e);return I([this.project(t.getSouthWest(),e)._subtract(r),this.project(t.getNorthWest(),e)._subtract(r),this.project(t.getSouthEast(),e)._subtract(r),this.project(t.getNorthEast(),e)._subtract(r)])},_getCenterLayerPoint:function(){return this.containerPointToLayerPoint(this.getSize()._divideBy(2))},_getCenterOffset:function(t){return this.latLngToLayerPoint(t).subtract(this._getCenterLayerPoint())},_limitCenter:function(t,e,n){if(!n)return t;var r=this.project(t,e),i=this.getSize().divideBy(2),a=new H(r.subtract(i),r.add(i)),o=this._getBoundsOffset(a,n,e);return o.round().equals([0,0])?t:this.unproject(r.add(o),e)},_limitOffset:function(t,e){if(!e)return t;var n=this.getPixelBounds(),r=new H(n.min.add(t),n.max.add(t));return t.add(this._getBoundsOffset(r,e))},_getBoundsOffset:function(t,e,n){var r=I(this.project(e.getNorthEast(),n),this.project(e.getSouthWest(),n)),i=r.min.subtract(t.min),a=r.max.subtract(t.max),o=this._rebound(i.x,-a.x),s=this._rebound(i.y,-a.y);return new P(o,s)},_rebound:function(t,e){return t+e>0?Math.round(t-e)/2:Math.max(0,Math.ceil(t))-Math.max(0,Math.floor(e))},_limitZoom:function(t){var e=this.getMinZoom(),n=this.getMaxZoom(),r=vt?this.options.zoomSnap:1;return r&&(t=Math.round(t/r)*r),Math.max(e,Math.min(n,t))},_onPanTransitionStep:function(){this.fire("move")},_onPanTransitionEnd:function(){_e(this._mapPane,"leaflet-pan-anim"),this.fire("moveend")},_tryAnimatedPan:function(t,e){var n=this._getCenterOffset(t)._trunc();return!(!0!==(e&&e.animate)&&!this.getSize().contains(n))&&(this.panBy(n,e),!0)},_createAnimProxy:function(){var t=this._proxy=le("div","leaflet-proxy leaflet-zoom-animated");this._panes.mapPane.appendChild(t),this.on("zoomanim",(function(t){var e=ie,n=this._proxy.style[e];Me(this._proxy,this.project(t.center,t.zoom),this.getZoomScale(t.zoom,1)),n===this._proxy.style[e]&&this._animatingZoom&&this._onZoomTransitionEnd()}),this),this.on("load moveend",this._animMoveEnd,this),this._on("unload",this._destroyAnimProxy,this)},_destroyAnimProxy:function(){ce(this._proxy),this.off("load moveend",this._animMoveEnd,this),delete this._proxy},_animMoveEnd:function(){var t=this.getCenter(),e=this.getZoom();Me(this._proxy,this.project(t,e),this.getZoomScale(e,1))},_catchTransitionEnd:function(t){this._animatingZoom&&t.propertyName.indexOf("transform")>=0&&this._onZoomTransitionEnd()},_nothingToAnimate:function(){return!this._container.getElementsByClassName("leaflet-zoom-animated").length},_tryAnimatedZoom:function(t,e,n){if(this._animatingZoom)return!0;if(n=n||{},!this._zoomAnimated||!1===n.animate||this._nothingToAnimate()||Math.abs(e-this._zoom)>this.options.zoomAnimationThreshold)return!1;var r=this.getZoomScale(e),i=this._getCenterOffset(t)._divideBy(1-1/r);return!(!0!==n.animate&&!this.getSize().contains(i))&&(T((function(){this._moveStart(!0,!1)._animateZoom(t,e,!0)}),this),!0)},_animateZoom:function(t,e,n,r){this._mapPane&&(n&&(this._animatingZoom=!0,this._animateToCenter=t,this._animateToZoom=e,me(this._mapPane,"leaflet-zoom-anim")),this.fire("zoomanim",{center:t,zoom:e,noUpdate:r}),setTimeout(i(this._onZoomTransitionEnd,this),250))},_onZoomTransitionEnd:function(){this._animatingZoom&&(this._mapPane&&_e(this._mapPane,"leaflet-zoom-anim"),this._animatingZoom=!1,this._move(this._animateToCenter,this._animateToZoom),T((function(){this._moveEnd(!0)}),this))}});function en(t,e){return new tn(t,e)}var nn=Y.extend({options:{position:"topright"},initialize:function(t){f(this,t)},getPosition:function(){return this.options.position},setPosition:function(t){var e=this._map;return e&&e.removeControl(this),this.options.position=t,e&&e.addControl(this),this},getContainer:function(){return this._container},addTo:function(t){this.remove(),this._map=t;var e=this._container=this.onAdd(t),n=this.getPosition(),r=t._controlCorners[n];return me(e,"leaflet-control"),-1!==n.indexOf("bottom")?r.insertBefore(e,r.firstChild):r.appendChild(e),this._map.on("unload",this.remove,this),this},remove:function(){return this._map?(ce(this._container),this.onRemove&&this.onRemove(this._map),this._map.off("unload",this.remove,this),this._map=null,this):this},_refocusOnMap:function(t){this._map&&t&&t.screenX>0&&t.screenY>0&&this._map.getContainer().focus()}}),rn=function(t){return new nn(t)};tn.include({addControl:function(t){return t.addTo(this),this},removeControl:function(t){return t.remove(),this},_initControlPos:function(){var t=this._controlCorners={},e="leaflet-",n=this._controlContainer=le("div",e+"control-container",this._container);function r(r,i){var a=e+r+" "+e+i;t[r+i]=le("div",a,n)}r("top","left"),r("top","right"),r("bottom","left"),r("bottom","right")},_clearControlPos:function(){for(var t in this._controlCorners)ce(this._controlCorners[t]);ce(this._controlContainer),delete this._controlCorners,delete this._controlContainer}});var an=nn.extend({options:{collapsed:!0,position:"topright",autoZIndex:!0,hideSingleBase:!1,sortLayers:!1,sortFunction:function(t,e,n,r){return n<r?-1:r<n?1:0}},initialize:function(t,e,n){for(var r in f(this,n),this._layerControlInputs=[],this._layers=[],this._lastZIndex=0,this._handlingClick=!1,t)this._addLayer(t[r],r);for(r in e)this._addLayer(e[r],r,!0)},onAdd:function(t){this._initLayout(),this._update(),this._map=t,t.on("zoomend",this._checkDisabledLayers,this);for(var e=0;e<this._layers.length;e++)this._layers[e].layer.on("add remove",this._onLayerChange,this);return this._container},addTo:function(t){return nn.prototype.addTo.call(this,t),this._expandIfNotCollapsed()},onRemove:function(){this._map.off("zoomend",this._checkDisabledLayers,this);for(var t=0;t<this._layers.length;t++)this._layers[t].layer.off("add remove",this._onLayerChange,this)},addBaseLayer:function(t,e){return this._addLayer(t,e),this._map?this._update():this},addOverlay:function(t,e){return this._addLayer(t,e,!0),this._map?this._update():this},removeLayer:function(t){t.off("add remove",this._onLayerChange,this);var e=this._getLayer(o(t));return e&&this._layers.splice(this._layers.indexOf(e),1),this._map?this._update():this},expand:function(){me(this._container,"leaflet-control-layers-expanded"),this._section.style.height=null;var t=this._map.getSize().y-(this._container.offsetTop+50);return t<this._section.clientHeight?(me(this._section,"leaflet-control-layers-scrollbar"),this._section.style.height=t+"px"):_e(this._section,"leaflet-control-layers-scrollbar"),this._checkDisabledLayers(),this},collapse:function(){return _e(this._container,"leaflet-control-layers-expanded"),this},_initLayout:function(){var t="leaflet-control-layers",e=this._container=le("div",t),n=this.options.collapsed;e.setAttribute("aria-haspopup",!0),Be(e),Fe(e);var r=this._section=le("section",t+"-list");n&&(this._map.on("click",this.collapse,this),rt||Pe(e,{mouseenter:this.expand,mouseleave:this.collapse},this));var i=this._layersLink=le("a",t+"-toggle",e);i.href="#",i.title="Layers",xt?(Pe(i,"click",$e),Pe(i,"click",this.expand,this)):Pe(i,"focus",this.expand,this),n||this.expand(),this._baseLayersList=le("div",t+"-base",r),this._separator=le("div",t+"-separator",r),this._overlaysList=le("div",t+"-overlays",r),e.appendChild(r)},_getLayer:function(t){for(var e=0;e<this._layers.length;e++)if(this._layers[e]&&o(this._layers[e].layer)===t)return this._layers[e]},_addLayer:function(t,e,n){this._map&&t.on("add remove",this._onLayerChange,this),this._layers.push({layer:t,name:e,overlay:n}),this.options.sortLayers&&this._layers.sort(i((function(t,e){return this.options.sortFunction(t.layer,e.layer,t.name,e.name)}),this)),this.options.autoZIndex&&t.setZIndex&&(this._lastZIndex++,t.setZIndex(this._lastZIndex)),this._expandIfNotCollapsed()},_update:function(){if(!this._container)return this;de(this._baseLayersList),de(this._overlaysList),this._layerControlInputs=[];var t,e,n,r,i=0;for(n=0;n<this._layers.length;n++)r=this._layers[n],this._addItem(r),e=e||r.overlay,t=t||!r.overlay,i+=r.overlay?0:1;return this.options.hideSingleBase&&(t=t&&i>1,this._baseLayersList.style.display=t?"":"none"),this._separator.style.display=e&&t?"":"none",this},_onLayerChange:function(t){this._handlingClick||this._update();var e=this._getLayer(o(t.target)),n=e.overlay?"add"===t.type?"overlayadd":"overlayremove":"add"===t.type?"baselayerchange":null;n&&this._map.fire(n,e)},_createRadioElement:function(t,e){var n='<input type="radio" class="leaflet-control-layers-selector" name="'+t+'"'+(e?' checked="checked"':"")+"/>",r=document.createElement("div");return r.innerHTML=n,r.firstChild},_addItem:function(t){var e,n=document.createElement("label"),r=this._map.hasLayer(t.layer);t.overlay?(e=document.createElement("input"),e.type="checkbox",e.className="leaflet-control-layers-selector",e.defaultChecked=r):e=this._createRadioElement("leaflet-base-layers_"+o(this),r),this._layerControlInputs.push(e),e.layerId=o(t.layer),Pe(e,"click",this._onInputClick,this);var i=document.createElement("span");i.innerHTML=" "+t.name;var a=document.createElement("div");n.appendChild(a),a.appendChild(e),a.appendChild(i);var s=t.overlay?this._overlaysList:this._baseLayersList;return s.appendChild(n),this._checkDisabledLayers(),n},_onInputClick:function(){var t,e,n=this._layerControlInputs,r=[],i=[];this._handlingClick=!0;for(var a=n.length-1;a>=0;a--)t=n[a],e=this._getLayer(t.layerId).layer,t.checked?r.push(e):t.checked||i.push(e);for(a=0;a<i.length;a++)this._map.hasLayer(i[a])&&this._map.removeLayer(i[a]);for(a=0;a<r.length;a++)this._map.hasLayer(r[a])||this._map.addLayer(r[a]);this._handlingClick=!1,this._refocusOnMap()},_checkDisabledLayers:function(){for(var t,e,n=this._layerControlInputs,r=this._map.getZoom(),i=n.length-1;i>=0;i--)t=n[i],e=this._getLayer(t.layerId).layer,t.disabled=void 0!==e.options.minZoom&&r<e.options.minZoom||void 0!==e.options.maxZoom&&r>e.options.maxZoom},_expandIfNotCollapsed:function(){return this._map&&!this.options.collapsed&&this.expand(),this},_expand:function(){return this.expand()},_collapse:function(){return this.collapse()}}),on=function(t,e,n){return new an(t,e,n)},sn=nn.extend({options:{position:"topleft",zoomInText:"+",zoomInTitle:"Zoom in",zoomOutText:"&#x2212;",zoomOutTitle:"Zoom out"},onAdd:function(t){var e="leaflet-control-zoom",n=le("div",e+" leaflet-bar"),r=this.options;return this._zoomInButton=this._createButton(r.zoomInText,r.zoomInTitle,e+"-in",n,this._zoomIn),this._zoomOutButton=this._createButton(r.zoomOutText,r.zoomOutTitle,e+"-out",n,this._zoomOut),this._updateDisabled(),t.on("zoomend zoomlevelschange",this._updateDisabled,this),n},onRemove:function(t){t.off("zoomend zoomlevelschange",this._updateDisabled,this)},disable:function(){return this._disabled=!0,this._updateDisabled(),this},enable:function(){return this._disabled=!1,this._updateDisabled(),this},_zoomIn:function(t){!this._disabled&&this._map._zoom<this._map.getMaxZoom()&&this._map.zoomIn(this._map.options.zoomDelta*(t.shiftKey?3:1))},_zoomOut:function(t){!this._disabled&&this._map._zoom>this._map.getMinZoom()&&this._map.zoomOut(this._map.options.zoomDelta*(t.shiftKey?3:1))},_createButton:function(t,e,n,r,i){var a=le("a",n,r);return a.innerHTML=t,a.href="#",a.title=e,a.setAttribute("role","button"),a.setAttribute("aria-label",e),Be(a),Pe(a,"click",$e),Pe(a,"click",i,this),Pe(a,"click",this._refocusOnMap,this),a},_updateDisabled:function(){var t=this._map,e="leaflet-disabled";_e(this._zoomInButton,e),_e(this._zoomOutButton,e),(this._disabled||t._zoom===t.getMinZoom())&&me(this._zoomOutButton,e),(this._disabled||t._zoom===t.getMaxZoom())&&me(this._zoomInButton,e)}});tn.mergeOptions({zoomControl:!0}),tn.addInitHook((function(){this.options.zoomControl&&(this.zoomControl=new sn,this.addControl(this.zoomControl))}));var un=function(t){return new sn(t)},ln=nn.extend({options:{position:"bottomleft",maxWidth:100,metric:!0,imperial:!0},onAdd:function(t){var e="leaflet-control-scale",n=le("div",e),r=this.options;return this._addScales(r,e+"-line",n),t.on(r.updateWhenIdle?"moveend":"move",this._update,this),t.whenReady(this._update,this),n},onRemove:function(t){t.off(this.options.updateWhenIdle?"moveend":"move",this._update,this)},_addScales:function(t,e,n){t.metric&&(this._mScale=le("div",e,n)),t.imperial&&(this._iScale=le("div",e,n))},_update:function(){var t=this._map,e=t.getSize().y/2,n=t.distance(t.containerPointToLatLng([0,e]),t.containerPointToLatLng([this.options.maxWidth,e]));this._updateScales(n)},_updateScales:function(t){this.options.metric&&t&&this._updateMetric(t),this.options.imperial&&t&&this._updateImperial(t)},_updateMetric:function(t){var e=this._getRoundNum(t),n=e<1e3?e+" m":e/1e3+" km";this._updateScale(this._mScale,n,e/t)},_updateImperial:function(t){var e,n,r,i=3.2808399*t;i>5280?(e=i/5280,n=this._getRoundNum(e),this._updateScale(this._iScale,n+" mi",n/e)):(r=this._getRoundNum(i),this._updateScale(this._iScale,r+" ft",r/i))},_updateScale:function(t,e,n){t.style.width=Math.round(this.options.maxWidth*n)+"px",t.innerHTML=e},_getRoundNum:function(t){var e=Math.pow(10,(Math.floor(t)+"").length-1),n=t/e;return n=n>=10?10:n>=5?5:n>=3?3:n>=2?2:1,e*n}}),cn=function(t){return new ln(t)},dn=nn.extend({options:{position:"bottomright",prefix:'`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/js/index.f644ce68.js](https://resorption-bidonvilles.beta.gouv.fr/js/index.f644ce68.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="link" onclick="createUser()">`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/robots.txt](https://resorption-bidonvilles.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="/js/chunk-vendors.8bba3be8.js"></script>`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr](https://resorption-bidonvilles.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="/js/chunk-vendors.8bba3be8.js"></script>`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/](https://resorption-bidonvilles.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="/js/chunk-vendors.8bba3be8.js"></script>`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/sitemap.xml](https://resorption-bidonvilles.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="/js/chunk-vendors.8bba3be8.js"></script>`
  
  
  
  
Instances: 6
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>Links have been found that do not have traditional href attributes, which is an indication that this is a modern web application.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Storable and Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, and may be retrieved directly from the cache, rather than from the origin server by the caching servers, in response to similar requests from other users.  If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where "shared" caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance.</p>
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js](https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr](https://resorption-bidonvilles.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/css/index.5be93f44.css](https://resorption-bidonvilles.beta.gouv.fr/css/index.5be93f44.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/css/chunk-vendors.da349212.css](https://resorption-bidonvilles.beta.gouv.fr/css/chunk-vendors.da349212.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/sitemap.xml](https://resorption-bidonvilles.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/img/favicon.ico](https://resorption-bidonvilles.beta.gouv.fr/img/favicon.ico)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/](https://resorption-bidonvilles.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/js/index.f644ce68.js](https://resorption-bidonvilles.beta.gouv.fr/js/index.f644ce68.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/robots.txt](https://resorption-bidonvilles.beta.gouv.fr/robots.txt)
  
  
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
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js](https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `0511287798`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js](https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `314245179`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/css/index.5be93f44.css](https://resorption-bidonvilles.beta.gouv.fr/css/index.5be93f44.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `17835908`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js](https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `18764656`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js](https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `23592600`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js](https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `15496570`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js](https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `2147483647`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js](https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `20037508`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js](https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `62425156`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js](https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `0511287776`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js](https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `999999975`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js](https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `40075017`
  
  
  
  
* URL: [https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js](https://resorption-bidonvilles.beta.gouv.fr/js/chunk-vendors.8bba3be8.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `94906265`
  
  
  
  
Instances: 13
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>0511287798, which evaluates to: 1986-03-15 16:23:18</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3