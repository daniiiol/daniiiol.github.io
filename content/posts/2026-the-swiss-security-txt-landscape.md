+++
authors = ["Dan"]
title = "The Swiss security.txt landscape in 2026"
date = "2026-02-01"
description = "Who's listening? security.txt adoption in Swiss cantons and municipalities"
images = [
    "/images/posts/hoheit_sectxt_2026_0201_2.png"
]
tags = [
    "security",
    "vulnerabilities",
    "security.txt",
    "information disclosure",
]
categories = [
    "Security",
    "Vulnerability Disclosure",
]
series = ["Ethical Hacking"]
+++

On 19 January 2023, the Swiss _National Cybersecurity Center_ (aka _BACS_) called on organisations to publish their security contact using `security.txt`.[^1] [^2]

Now, roughly three years after that publication, I wanted to take a look at how many Swiss cantons and municipalities have followed this recommendation.


{{< notice info >}}
In short, a _security.txt_ is a small text file that organisations usually publish on their website at `https://<myUrl>.domain/.well-known/security.txt`.

People who have discovered a vulnerability - or at least suspect one - can find the preferred contact channel for responsible disclosure in this file. This allows vulnerabilities to be reported in a controlled and as targeted a manner as possible.

More information about _security.txt_ can be found in the corresponding specification, [RFC 9116](https://www.rfc-editor.org/rfc/rfc9116.html). If you prefer a simpler approach and want to quickly generate such a text file, you can for example use this helper page: [https://securitytxt.org/](https://securitytxt.org/)

{{< /notice >}}

# Status of the cantons

When I started this small research project, I actually assumed that all Swiss cantons would have followed this security recommendation. We are confronted with vulnerabilities and attacks on a daily basis, and with ongoing digitalisation the threat landscape for cantonal organisations and their citizens continues to grow. In addition, due to its national mandate, the NCSC typically keeps a close eye on the cantons, and publishing a security contact does not exactly feel like a mammoth task.

The outcome of the analysis looked as follows:

<a href="/attachements/posts/securitytxt/cantons.html" target="_blank">![Overview of all cantons with a published security.txt (green)](/images/posts/kanton_sectxt_2026_0201.png)</a>

As of 2026, 21 out of 26 Swiss cantons have published a corresponding security contact. Solothurn, Schaffhausen, both Appenzell cantons, and Vaud do not provide any guidance for security-related contact. The _security.txt_ files also implicitly reveal which cantons may be better prepared against cyber attacks: those that list a dedicated Cantonal authority as their contact point. Some cantons, however, rely exclusively on their website service provider for handling security reports. At least, this is the first point of contact specified for vulnerabilities within the canton.

The full breakdown is shown again in the following table:

| Canton                 | security.txt | VDP/CVD | Contact                        |
| ---------------------- | ------------ | ------- | ------------------------------ |
| Aargau                 | ✅            | ✅       | Cantonal authority |
| Appenzell Ausserrhoden | ❌            | ❌       | –                              |
| Appenzell Innerrhoden  | ❌            | ❌       | –                              |
| Basel-Landschaft       | ✅            | ❌       | Webcloud7                      |
| Basel-Stadt            | ✅            | ❌       | Cantonal authority |
| Bern                   | ✅            | ✅       | Cantonal authority |
| Fribourg               | ✅            | ❌       | Cantonal authority |
| Geneva                 | ✅            | ✅       | Cantonal authority |
| Glarus                 | ✅            | ❌       | Backslash                      |
| Grisons                | ✅            | ❌       | Cantonal authority |
| Jura                   | ✅            | ✅       | Cantonal authority |
| Lucerne                | ✅            | ✅       | Cantonal authority |
| Neuchâtel              | ✅            | ❌       | Cantonal authority |
| Nidwalden              | ✅            | ❌       | i-Web                          |
| Obwalden               | ✅            | ❌       | i-Web                          |
| Schaffhausen           | ❌            | ❌       | –                              |
| Schwyz                 | ✅            | ❌       | Cantonal authority |
| Solothurn              | ❌            | ❌       | –                              |
| St.Gallen              | ✅            | ❌       | Cantonal authority |
| Thurgau                | ✅            | ❌       | Backslash                      |
| Ticino                 | ✅            | ❌       | Cantonal authority |
| Uri                    | ✅            | ❌       | i-Web                          |
| Valais                 | ✅            | ✅       | Cantonal authority |
| Vaud                   | ❌            | ❌       | –                              |
| Zug                    | ✅            | ❌       | Cantonal authority |
| Zurich                 | ✅            | ✅       | Cantonal authority |



# Status of the municipalities

The picture looks somewhat more differentiated at the municipal level. Out of 2,110 municipalities in Switzerland (as of 1 January 2026), only 880 have published a _security.txt_. The majority of these files are actually provided by the website operator[^3] themselves.

I tried to identify as many municipalities as possible. However, determining the official websites of Swiss municipalities turned out to be more challenging than initially expected, as there is no formal requirement or standard for municipal URLs in Switzerland. That said, the overall coverage of municipal websites was higher than anticipated. I was only unable to identify the websites of three municipalities (Rebévelier, Kammersrohr, and Mettembert). Any helpful hints are of course welcome.

**Fun fact:** There are also three municipalities in Switzerland that have still not migrated to HTTPS (secure communication with the web server). I will refrain from naming them here - maybe I'll need that for a quiz one day. 😉

The following image shows the overall situation for security contacts at the municipal level:

<a href="/attachements/posts/securitytxt/municipalities.html" target="_blank">![Overview of all municipalities with a published security.txt (green)](/images/posts/hoheit_sectxt_2026_0201_2.png)</a>

{{< notice tip >}}
Click on the image to open the interactive map. 
{{< /notice >}}


# Conclusion

Cantons and municipalities certainly have more important tasks than publishing a security contact on the internet. In practice, it is often still possible to reach the right people through other channels or, as a last resort, to contact the NCSC via its general reporting form.[^4]

However, the absence of a _security.txt_ should not be dismissed as a minor oversight. Publishing such a file is basic security hygiene. It requires no complex architecture, no additional infrastructure, and virtually no budget. What it does require is clear ownership and responsibility. When even this minimal mechanism is missing, it raises questions about the prioritisation of operational security processes.

At the same time, the presence of a _security.txt_ alone does not imply effective incident response or mature security operations. Nevertheless, the content of these files provides meaningful signals. Cantons that list a dedicated internal security organisation as their point of contact demonstrate a higher level of organisational readiness. Cantons that rely solely on external web service providers appear to treat vulnerability handling as a peripheral concern rather than a core responsibility.

Viewed in this way, _security.txt_ is less a compliance checkbox and more a simple indicator of security awareness and process maturity. For municipalities, the current level of adoption is partly understandable given structural and resource constraints. For the cantons, full adoption would be both realistic and desirable. I would genuinely like to see a 100% adoption rate by the end of 2026.


[^1]: cf. _NCSC - Include your security contact on your website_, [https://www.ncsc.admin.ch/ncsc/en/home/aktuell/im-fokus/2023/security_txt.html](https://www.ncsc.admin.ch/ncsc/en/home/aktuell/im-fokus/2023/security_txt.html), accessed 2026-01-31
[^2]: cf. _NCSC - security.txt - Include your security contact on your website_, [https://www.ncsc.admin.ch/ncsc/en/home/infos-fuer/infos-unternehmen/aktuelle-themen/security-txt.html](https://www.ncsc.admin.ch/ncsc/en/home/infos-fuer/infos-unternehmen/aktuelle-themen/security-txt.html), accessed 2026-01-31
[^3]: **i-Web**: 485 | **Backslash**: 248 | **Talus**: 64 | **o-i.ch**: 11 | **Others**: 72
[^4]: cf. _NCSC - Coordinated Vulnerability Disclosure (CVD)_, [https://www.ncsc.admin.ch/ncsc/en/home/infos-fuer/infos-it-spezialisten/themen/schwachstelle-melden.html](https://www.ncsc.admin.ch/ncsc/en/home/infos-fuer/infos-it-spezialisten/themen/schwachstelle-melden.html), accessed 2026-01-31