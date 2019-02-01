---
layout: post
title: "Useful Firefox config changes"
date: 2018-10-29
---

In order to minimize the risk of having the browser hide or mitigate vulnerabilities when testing its useful to alter the default browser configuration somewhat.
I got a few new suggestions from watching a SANS webcast on using Burp Suite for web hacking a few days ago where [Chris Dale](https://twitter.com/chrisadale) shared many great tips.
I strongly recommend watching the entire [webcast](https://www.sans.org/webcasts/web-hacking-burp-suite-deep-dive-burp-suites-functionality-pen-testers-108860) if the topic applies to you.

Unfortunately there doesn't seem to be a good way to export just the configuration changes from Firefox for sharing. I haven't found any at least.  
Here is a short list on some changes I recommend doing in about:config.

##### Disable Normandy (feedback to Mozilla)
```
app.normandy.enabled = false 
```
##### Disable SafeBrowsing
```
browser.safebrowsing.blockedURIs.enabled = false
browser.safebrowsing.downloads.enabled = false
browser.safebrowsing.downloads.remote.enabled = false
browser.safebrowsing.malware = false
browser.safebrowsing.phishing = false
```
##### Disable automatic browse suggestions
```
browser.urlbar.filter.autocomplete = false
```
##### Disable Activity Stream
```
browser.library.activity-stream.enabled = false
browser.newtabpage.activity-stream.feeds.telemetry = false
browser.newtabpage.activity-stream.telemetry = false
```
##### Disable XSS protection
```
browser.urlbar.filter.javascript = false
```
##### Disable health report
```
datareporting.healthreport.uploadEnabled = false
```
##### Disable captive portal
```
network.captive-portal-service = false
```
##### Disable flash block
```
plugins.flashBlock.enabled = false
```
##### Disable tracking protection
```
privacy.trackingprotection.annotate_channels = false
privacy.trackingprotection.enabled = false
privacy.trackingprotection.pbmode.enabled = false
```
##### Allow mixed context
```
security.mixed_content.block_active_content = false
```
##### Disable OCSP stapling
```
security.ssl.enable_ocsp_stapling = false
```
##### Disable ssl error reporting
```
security.ssl.errorReporting.enabled = false
```
##### Allow weak ciphers
```
security.tls.version.min = 0
```
##### Disable even more telemetry
```
toolkit.telemetry.archive.enabled = false
toolkit.telemetry.enabled = false
browser.ping-centre.telemetry = false
```



