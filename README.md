# Content-Security-Policy-CSP-Bypass-Techniques
Content-Security-Policy (CSP) Bypass Techniques

# What is a CSP ?
CSP stands for Content Security Policy which is a mechanism to define which resources can be fetched out or executed by a web page. In other words, it can be understood as a policy that decides which scripts, images, iframes can be called or executed on a particular page from different locations. Content Security Policy is implemented via response headers or meta elements of the HTML page. From there, it’s browser’s call to follow that policy and actively block violations as they are detected.

# Why it is used?
Content Security Policy is widely used to secure web applications against content injection like cross-site scripting attacks. Also by using CSP the server can specify which protocols are allowed to be used. Can we think CSP as mitigation of XSS? The answer is no! CSP is an extra layer of security against content injection attacks. The first line of defense is output encoding and input validation always. A successful CSP implementation not only secures a web page against these vulnerabilities but also gives a wide range of attack details that were unsuccessful i.e. blocked by CSP itself. Web admin can be benefitted using this feature to spot a potential bug.


# How does it work?
CSP works by restricting the origins that active and passive content can be loaded from. It can additionally restrict certain aspects of active content such as the execution of inline JavaScript, and the use of eval().

If you are a developer you will require to define all allowed origins for every type of resource your website utilizes. Suppose you are the owner of a website abc.com and these websites loads multiple resources like scripts, images, css from localhost, and different sources as well, say allowed.com. A very basic policy would be :

# Implemented via Response Header:
