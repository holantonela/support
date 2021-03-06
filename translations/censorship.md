_model: question
---
title: Our website is blocked by a censor. Can Tor Browser help users access our website?
---
seo_slug: our-website-is-blocked-by-a-censor
---
description:
<p class="mb-3">Tor Browser can certainly help people access your website in places where it is blocked. Most of the time, simply downloading the ​<mark><a href="https://www.torproject.org/download/download-easy.html.en">Tor Browser</a></mark> and then using it to navigate to the blocked site will allow access. In places where there is heavy censorship we have a number of censorship circumvention options available, including ​<mark><a href="https://www.torproject.org/docs/pluggable-transports.html.en">pluggable transports</a></mark>. For more information, please see the <mark><a href="https://tb-manual.torproject.org/en-US/">​Tor Browser User Manual</a></mark> section on <mark><a href="https://tb-manual.torproject.org/en-US/circumvention.html">censorship</a></mark>.</p>


_model: question
---
title: I can’t connect to Tor Browser, is my network censored?
---
seo_slug: cant-connect-to-tor-browser
---
description:
<p class="mb-3">You might be on a censored network, and so you should try using bridges. Some bridges are built in to Tor Browser, and you can use those bridges by choosing "configure" (then following the prompts) in the Tor Launcher window that pops up when you open Tor Browser for the first time. If you need other bridges, you can get them at our ​<mark><a href="https://bridges.torproject.org/">Bridges website</a></mark>. For more information about bridges, see the <mark><a href="https://tb-manual.torproject.org/en-US/bridges.html">​Tor Browser manual</a></mark>.</p>

_model: question
---
title: How do I download Tor if the torproject.org is blocked?
---
seo_slug: how-do-i-download-tor-if-torproject-org-is-blocked
---
description:

<p class="mb-3">If you can't download Tor through our ​<mark><a href=\"https://www.torproject.org\">website</a></mark>, you can get a copy of Tor delivered to you via GetTor. GetTor is a service that automatically responds to messages with links to the latest version of Tor Browser, hosted at a variety of locations that are less likely to be censored, such as Dropbox, Google Drive, and Github.</p>

_model: question
---
title: A website I am trying to reach is blocking access over Tor.
---
seo_slug: website-is-blocking-access-over-tor
---
description:
<p class="mb-3">Sometimes websites will block Tor users because they can't tell the difference between the average Tor user and automated traffic. The best success we've had in getting sites to unblock Tor users is getting users to contact the site administrators directly. Something like this might do the trick:
<br />
"Hi! I tried to access your site xyz.com while using Tor Browser and discovered that you don't allow Tor users to access your site. I urge you to reconsider this decision; Tor is used by people all over the world to protect their privacy and fight censorship. By blocking Tor users, you are likely blocking people in repressive countries who want to use a free internet, journalists and researchers who want to protect themselves from discovery, whistleblowers, activists, and ordinary people who want to opt out of invasive third party tracking. Please take a strong stance in favor of digital privacy and internet freedom, and allow Tor users access to xyz.com. Thank you."
<br />
In the case of banks, and other sensitive websites, it is also common to see geography-based blocking (if a bank knows you generally access their services from one country, and suddenly you are connecting from an exit relay on the other side of the world, your account may be locked or suspended). If you are unable to connect to an onion service, please see <a href="#onionservices-3">I cannot reach X.onion!</a></p>


_model: question
---
title: I am having trouble connecting to Tor, and I can’t figure out what’s wrong.
---
seo_slug: having-trouble-connecting-to-tor
---
description:
<p class="mb-3">If you’re having trouble connecting, please select the option to "copy Tor log to clipboard." Then paste the Tor log into a text file or other document. You should see one of these common log errors (look for the following lines in your Tor log):</p>
<h5>Common log error #1: Proxy connection failure</h5>
<p class="mb-3">
<pre>
<code>
2017-10-29 09:23:40.800 [NOTICE] Opening Socks listener on 127.0.0.1:9150
2017-10-29 09:23:47.900 [NOTICE] Bootstrapped 5%: Connecting to directory server
2017-10-29 09:23:47.900 [NOTICE] Bootstrapped 10%: Finishing handshake with directory server
2017-10-29 09:24:08.900 [WARN] Proxy Client: unable to connect to xx..xxx..xxx.xx:xxxxx ("general SOCKS server failure")
2017-10-29 09:24:08.900 [WARN] Proxy Client: unable to connect to xx..xxx..xxx.xx:xxxxx  ("general SOCKS server failure")
2017-10-29 09:24:08.900 [WARN] Proxy Client: unable to connect toxx..xxx..xxx.xx:xxxxx  ("general SOCKS server failure")
</code>
</pre>
</p>
<p class="mb-3">If you see lines like these  in your Tor log, it means you are failing to connect to a SOCKS proxy. If a SOCKS proxy is required for your network setup, then please make sure you’ve entered your proxy details correctly.  If a SOCKS proxy is not required, or you’re not sure,  please try connecting to the Tor network without a SOCKS proxy.</p>
<h5>Common log error #2: Can’t reach guard relays</h5>
<p class="mb-3">
<pre>
<code>
11/1/2017 21:11:43 PM.500 [NOTICE] Opening Socks listener on 127.0.0.1:9150
11/1/2017 21:11:44 PM.300 [NOTICE] Bootstrapped 80%: Connecting to the Tor network
11/1/2017 21:11:44 PM.300 [WARN] Failed to find node for hop 0 of our path. Discarding this circuit.
11/1/2017 21:11:44 PM.500 [NOTICE] Bootstrapped 85%: Finishing handshake with first hop
11/1/2017 21:11:45 PM.300 [WARN] Failed to find node for hop 0 of our path. Discarding this circuit.
</code>
</pre>
</p>
<p class="mb-3">
If you see lines like these in your Tor log, it means your Tor failed to connect to the first node in the Tor circuit. This could mean that you’re on a network that’s censored. Please try connecting with bridges, and that should fix the problem.</p>
<h5>Common log error #3: Failed to complete TLS handshake</h5>
<p class="mb-3">
<pre>
<code>
13-11-17 19:52:24.300 [NOTICE] Bootstrapped 10%: Finishing handshake with directory server
13-11-17 19:53:49.300 [WARN] Problem bootstrapping. Stuck at 10%: Finishing handshake with directory server. (DONE; DONE; count 10; recommendation warn; host [host] at xxx.xxx.xxx.xx:xxx)
13-11-17 19:53:49.300 [WARN] 10 connections have failed:
 13-11-17 19:53:49.300 [WARN]  9 connections died in state handshaking (TLS) with SSL state SSLv2/v3 read server hello A in HANDSHAKE
13-11-17 19:53:49.300 [WARN]  1 connections died in state connect()ing with SSL state (No SSL object)
</code>
</pre>
</p>
<p class="mb-3">If you see lines like this in your Tor log, it means that Tor failed to complete a TLS handshake with the directory authorities. Using bridges will likely fix this.</p>
<h5>Common log error #4: Clock skew</h5>
<p class="mb-3">
<pre>
<code>
19.11.2017 00:04:47.400 [NOTICE] Opening Socks listener on 127.0.0.1:9150
19.11.2017 00:04:48.000 [NOTICE] Bootstrapped 5%: Connecting to directory server
19.11.2017 00:04:48.200 [NOTICE] Bootstrapped 10%: Finishing handshake with directory server
19.11.2017 00:04:48.800 [WARN] Received NETINFO cell with skewed time (OR:xxx.xx.x.xx:xxxx): It seems that our clock is behind by 1 days, 0 hours, 1 minutes, or that theirs is ahead.
Tor requires an accurate clock to work: please check your time, timezone, and date settings.
</code>
</pre>
</p>
<p class="mb-3">If you see lines like this in your Tor log, it means your system clock is incorrect. Please make sure your clock is set accurately, including the correct timezone. Then restart Tor. </p>

_model: topic
---
title: Censorship
---
seo_slug: censorship
---
key:7
---


_model: question
---
title: I can’t connect to Tor Browser, is my network censored?
---
seo_slug: is-my-network-censored
---
description:
<p class="mb-3">You might be on a censored network, and so you should try using bridges. Some bridges are built in to Tor Browser, and you can use those bridges by choosing "configure" (then following the prompts) in the Tor Launcher window that pops up when you open Tor Browser for the first time. If you need other bridges, you can get them at our ​<mark><a href="https://bridges.torproject.org/">Bridges website</a></mark>. For more information about bridges, see the <mark><a href="https://tb-manual.torproject.org/en-US/bridges.html">​Tor Browser manual</a></mark>.</p>

_model: question
---
title: Our website is blocked by a censor. Can Tor Browser help users access our website?
---
seo_slug: our-website-is-blocked-by-a-censor
---
description:

<p class="mb-3">Tor Browser can certainly help people access your website in places where it is blocked. Most of the time, simply downloading the ​<mark><a href="https://www.torproject.org/download/download-easy.html.en">Tor Browser</a></mark> and then using it to navigate to the blocked site will allow access. In places where there is heavy censorship we have a number of censorship circumvention options available, including ​<mark><a href="https://www.torproject.org/docs/pluggable-transports.html.en">pluggable transports</a></mark>. For more information, please see the <mark><a href="https://tb-manual.torproject.org/en-US/">​Tor Browser User Manual</a></mark> section on <mark><a href="https://tb-manual.torproject.org/en-US/circumvention.html">censorship</a></mark>.</p>


_model: question
---
title: I can’t connect to Tor Browser, is my network censored?
---
seo_slug: cant-connect-to-tor-browser
---
description:
<p class="mb-3">You might be on a censored network, and so you should try using bridges. Some bridges are built in to Tor Browser, and you can use those bridges by choosing "configure" (then following the prompts) in the Tor Launcher window that pops up when you open Tor Browser for the first time. If you need other bridges, you can get them at our ​<mark><a href="https://bridges.torproject.org/">Bridges website</a></mark>. For more information about bridges, see the <mark><a href="https://tb-manual.torproject.org/en-US/bridges.html">​Tor Browser manual</a></mark>.</p>

_model: question
---
title: How do I download Tor if the torproject.org is blocked?
---
seo_slug: how-do-i-download-tor-if-torproject-org-is-blocked
---
description:

<p class="mb-3">If you can't download Tor through our ​<mark><a href=\"https://www.torproject.org\">website</a></mark>, you can get a copy of Tor delivered to you via GetTor. GetTor is a service that automatically responds to messages with links to the latest version of Tor Browser, hosted at a variety of locations that are less likely to be censored, such as Dropbox, Google Drive, and Github.</p>

_model: question
---
title: A website I am trying to reach is blocking access over Tor.
---
seo_slug: website-is-blocking-access-over-tor
---
description:
<p class="mb-3">Sometimes websites will block Tor users because they can't tell the difference between the average Tor user and automated traffic. The best success we've had in getting sites to unblock Tor users is getting users to contact the site administrators directly. Something like this might do the trick:
<br />
"Hi! I tried to access your site xyz.com while using Tor Browser and discovered that you don't allow Tor users to access your site. I urge you to reconsider this decision; Tor is used by people all over the world to protect their privacy and fight censorship. By blocking Tor users, you are likely blocking people in repressive countries who want to use a free internet, journalists and researchers who want to protect themselves from discovery, whistleblowers, activists, and ordinary people who want to opt out of invasive third party tracking. Please take a strong stance in favor of digital privacy and internet freedom, and allow Tor users access to xyz.com. Thank you."
<br />
In the case of banks, and other sensitive websites, it is also common to see geography-based blocking (if a bank knows you generally access their services from one country, and suddenly you are connecting from an exit relay on the other side of the world, your account may be locked or suspended). If you are unable to connect to an onion service, please see <a href="#onionservices-3">I cannot reach X.onion!</a></p>


_model: question
---
title: I am having trouble connecting to Tor, and I can’t figure out what’s wrong.
---
seo_slug: having-trouble-connecting-to-tor
---
description:
<p class="mb-3">If you’re having trouble connecting, please select the option to "copy Tor log to clipboard." Then paste the Tor log into a text file or other document. You should see one of these common log errors (look for the following lines in your Tor log):</p>
<h5>Common log error #1: Proxy connection failure</h5>
<p class="mb-3">
<pre>
<code>
2017-10-29 09:23:40.800 [NOTICE] Opening Socks listener on 127.0.0.1:9150
2017-10-29 09:23:47.900 [NOTICE] Bootstrapped 5%: Connecting to directory server
2017-10-29 09:23:47.900 [NOTICE] Bootstrapped 10%: Finishing handshake with directory server
2017-10-29 09:24:08.900 [WARN] Proxy Client: unable to connect to xx..xxx..xxx.xx:xxxxx ("general SOCKS server failure")
2017-10-29 09:24:08.900 [WARN] Proxy Client: unable to connect to xx..xxx..xxx.xx:xxxxx  ("general SOCKS server failure")
2017-10-29 09:24:08.900 [WARN] Proxy Client: unable to connect toxx..xxx..xxx.xx:xxxxx  ("general SOCKS server failure")
</code>
</pre>
</p>
<p class="mb-3">If you see lines like these  in your Tor log, it means you are failing to connect to a SOCKS proxy. If a SOCKS proxy is required for your network setup, then please make sure you’ve entered your proxy details correctly.  If a SOCKS proxy is not required, or you’re not sure,  please try connecting to the Tor network without a SOCKS proxy.</p>
<h5>Common log error #2: Can’t reach guard relays</h5>
<p class="mb-3">
<pre>
<code>
11/1/2017 21:11:43 PM.500 [NOTICE] Opening Socks listener on 127.0.0.1:9150
11/1/2017 21:11:44 PM.300 [NOTICE] Bootstrapped 80%: Connecting to the Tor network
11/1/2017 21:11:44 PM.300 [WARN] Failed to find node for hop 0 of our path. Discarding this circuit.
11/1/2017 21:11:44 PM.500 [NOTICE] Bootstrapped 85%: Finishing handshake with first hop
11/1/2017 21:11:45 PM.300 [WARN] Failed to find node for hop 0 of our path. Discarding this circuit.
</code>
</pre>
</p>
<p class="mb-3">
If you see lines like these in your Tor log, it means your Tor failed to connect to the first node in the Tor circuit. This could mean that you’re on a network that’s censored. Please try connecting with bridges, and that should fix the problem.</p>
<h5>Common log error #3: Failed to complete TLS handshake</h5>
<p class="mb-3">
<pre>
<code>
13-11-17 19:52:24.300 [NOTICE] Bootstrapped 10%: Finishing handshake with directory server
13-11-17 19:53:49.300 [WARN] Problem bootstrapping. Stuck at 10%: Finishing handshake with directory server. (DONE; DONE; count 10; recommendation warn; host [host] at xxx.xxx.xxx.xx:xxx)
13-11-17 19:53:49.300 [WARN] 10 connections have failed:
 13-11-17 19:53:49.300 [WARN]  9 connections died in state handshaking (TLS) with SSL state SSLv2/v3 read server hello A in HANDSHAKE
13-11-17 19:53:49.300 [WARN]  1 connections died in state connect()ing with SSL state (No SSL object)
</code>
</pre>
</p>
<p class="mb-3">If you see lines like this in your Tor log, it means that Tor failed to complete a TLS handshake with the directory authorities. Using bridges will likely fix this.</p>
<h5>Common log error #4: Clock skew</h5>
<p class="mb-3">
<pre>
<code>
19.11.2017 00:04:47.400 [NOTICE] Opening Socks listener on 127.0.0.1:9150
19.11.2017 00:04:48.000 [NOTICE] Bootstrapped 5%: Connecting to directory server
19.11.2017 00:04:48.200 [NOTICE] Bootstrapped 10%: Finishing handshake with directory server
19.11.2017 00:04:48.800 [WARN] Received NETINFO cell with skewed time (OR:xxx.xx.x.xx:xxxx): It seems that our clock is behind by 1 days, 0 hours, 1 minutes, or that theirs is ahead.
Tor requires an accurate clock to work: please check your time, timezone, and date settings.
</code>
</pre>
</p>
<p class="mb-3">If you see lines like this in your Tor log, it means your system clock is incorrect. Please make sure your clock is set accurately, including the correct timezone. Then restart Tor. </p>

_model: question
---
title: I can’t connect to Tor Browser, is my network censored?
---
seo_slug: is-my-network-censored
---
description:
<p class="mb-3">You might be on a censored network, and so you should try using bridges. Some bridges are built in to Tor Browser, and you can use those bridges by choosing "configure" (then following the prompts) in the Tor Launcher window that pops up when you open Tor Browser for the first time. If you need other bridges, you can get them at our ​<mark><a href="https://bridges.torproject.org/">Bridges website</a></mark>. For more information about bridges, see the <mark><a href="https://tb-manual.torproject.org/en-US/bridges.html">​Tor Browser manual</a></mark>.</p>


_model: question
---
title: What is a bridge?
---
seo_slug: what-is-a-bridge
---
description:
<p class="mb-3">Bridge relays are Tor relays that are not listed in the public Tor directory. That means that ISPs or governments trying to block access to the Tor network can't simply block all bridges. Bridges are useful for Tor users under oppressive regimes, and for people who want an extra layer of security because they're worried somebody will recognize that they are contacting a public Tor relay IP address.</p><p class="mb-3">A bridge is just a normal relay with a slightly different configuration. See (link to How do I run a bridge) for instructions.</p><p class="mb-3">Several countries, including China and Iran, have found ways to detect and block connections to Tor bridges. <mark>​<a href="https://github.com/Yawning/obfs4/blob/master/doc/obfs4-spec.txt">Obfsproxy</a></mark> bridges address this by adding another layer of obfuscation.</p><p class="mb-3">Setting up an obfsproxy bridge requires an additional software package and additional configurations. See ​our page on <mark><a href="https://www.torproject.org/docs/pluggable-transports.html.en">pluggable transports</a></mark> for more info.</p>
