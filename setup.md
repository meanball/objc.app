#### GitBook

`gitbook build`

then copy to objc_app_domain folder

####GA

```
<!-- Global site tag (gtag.js) - Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=UA-15706253-19"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'UA-15706253-19');
</script>
``` 

#### Add google adsense

put inbetween <head> </head>

```
<script async src="//pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script>
<script>
     (adsbygoogle = window.adsbygoogle || []).push({
          google_ad_client: "ca-pub-1312390534229992",
          enable_page_level_ads: true
     });
</script>
```
