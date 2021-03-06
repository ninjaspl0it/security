# Passive Information Gatherig

It is passive in the meaning that it doesn't directly send packets to the service. But in any other sense of the word there is nothing passive about this phase.

## Visit the website <a id="visit-the-website"></a>

Okay, I guess this actually sends packets to the target, but whatever. Visit the page, look around, read about the target. What do they do?

## Whois <a id="whois"></a>

Find out who is behind the website.

Resolve the DNS

```text
host website.com
nslookup website.com
```

The the IP address and check it with `whois`

```text
whois 192.168.1.101
```

## Netcraft <a id="netcraft"></a>

Most of the info found on netcraft is not unique. It is basic whois info. But one thing is really good, it lists the different IP-addresses the page has had over the years. This can be a good way to **bypass cloudflare** and other services that hide the real IP. Using netcraft we can find the IP that was in use before they implemented cloudflare.

Another detail that is good to know is the **hosting-company** or **domain-provider**. Those details can be used if we want to try some **social-engineering or spear-phishing attack**.

[Netcraft](https://www.netcraft.com/)

## References <a id="references"></a>

[http://www.technicalinfo.net/papers/PassiveInfoPart1.html](http://www.technicalinfo.net/papers/PassiveInfoPart1.html)

