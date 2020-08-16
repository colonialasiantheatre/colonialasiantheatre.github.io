---
layout: default
title: Home
---

## About

This website features students' original pieces of historical writing on histories of colonial South, Southeast, and East Asian theatre during the nineteenth and early twentieth centuries.

[See more...](/about)

![](/assets/home1.webp){: style="margin: 0 auto;"}
<p class="right" style="font-size: 80%">1828 Map of Asia from F. D. Zachary, Public Domain</p>

<hr>

## Student Works

{% for post in site.tags.preview %}
-  [{{ post.title }}]({{ post.url }})
{% endfor %}

[See more...](/studentworks)

<hr>

<div id="resources"></div>
## Resources

[Delpher][1] - Digitised Dutch East Indies newspapers, books, and magazines

[NewspaperSG][2] - An online digital archive of Singapore's newspapers

[Digitised HK Newspapers][3] - Digitised archive of old HK newspapers

[Asiatic Society of Mumbai][4] - Digitised books, newspapers, manuscripts, maps, journals, government publications and reports from colonial India.

[ProQuest Historical Newspaper][5] ([Chinese Newspaper][6] / [SCMP][7]) - Expansive digital archive of historical newspapers

[HKUL Special Collections][8] ([Digital][9])

[1]: https://www.delpher.nl/
[2]: https://eresources.nlb.gov.sg/newspapers/
[3]: https://eresources.nlb.gov.sg/newspapers/
[4]: https://www.granthsanjeevani.com/jspui/
[5]: https://about.proquest.com/products-services/pq-hist-news.html
[6]: https://search-proquest-com.eproxy.lib.hku.hk/hnpchinesecollection/news/fromDatabasesLayer/databases
[7]: https://search-proquest-com.eproxy.lib.hku.hk/hnpsouthchinamorningpost/databases?accountid=14548
[8]: https://lib.hku.hk/hkspc/collections.html
[9]: https://lib.hku.hk/hkspc/HK-Studies.html
