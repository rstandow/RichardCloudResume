---
title: 'test'
date: Thu, 01 Jan 2009 14:09:10 +0000
draft: false
tags: [apache, apache, redirect, rewrite, ssl, web development]
---

Intro
-----

Doesn't matter whether it's a CakePHP app for a client, your own personal CMS, or any other web based application. **If your passing around passwords or other sensitive info you should really implement SSL.** SSL provides 2 main perks to your visitors.

*   First it encrypts all communication that flies across the web. This prevents curious or devious billies from getting your secrets.
*   Secondly it ensures to the user that your server is in fact who it claims, and not a nasty 'man in the middle" attack.
*   Finally it gives your site that touch of class.... which of course a classy person like yourself relies on.

Once you implement SSL certificates on your server you'll want to **require secure connections** using Apache's rewrite module. Now I won't dwell on the creation and signing of certificates, its already well documented.  If your just starting out though,heres a few links I recommend;

*   [Creating self-signed certificates](http://www.tc.umn.edu/~brams006/selfsign.html "Creating and Signing your own SSL Certificate") (free, but should only be used internally or for testing, users will; see an 'Untrusted" warning)
*   [Requesting a CA Signed certificate](http://www.google.com/url?sa=t&source=web&ct=res&cd=10&url=http%3A%2F%2Fwww.lsu.edu%2Fpki%2FSSL_Certificate_Apache.pdf&ei=Z8FcSbDRGaCY8gTdk7GHDQ&usg=AFQjCNELddGd6jW1_Dv1X-CaocEVa4rV2A&sig2=FQMNaM_RlhngJW3MSYiQzw "Generating a Certificate Signing Request") (not free, but the final certificate is trusted and seamless for users)

The second link uses the schools internal CA, you will need to pay a public CA like Entrust or Verisign. **All of this information is aimed at 'nix or solaris servers running apache**. Why? cause a production windows server is laughable :-p

Now that you have a certificate, whats next?
--------------------------------------------

So there you are you have a shiny new Certificate and Server key, how do you force visitors to your apache driven site to use the SSL? You copied the certificates into the appropite locations right? And you have made the needed changes in httpd.conf right? So now when you view https://example.com you see a 'trusted' warning or your site right? If No to any of these than [this article](http://www.sitepoint.com/article/securing-apache-2-server-ssl/ "Securing Apcche Server with SSL") does a pretty good job of outlining those steps.

The SSL Works, How do I force connections to use it?
----------------------------------------------------

