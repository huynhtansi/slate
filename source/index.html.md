---
title: DinoAd API Reference

language_tabs:
  - shell

toc_footers:
  - <a href='https://github.com/huynhtansi'>Documentation Powered by HTSI</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the DinoAd API! You can use our API to access Dino Adserver API endpoints, which can get information on various advertisers, campaigns, and banners in our database.

> To authorize, use this code:

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: <Authentication Key>"
```
# Banners

## Get All Banners

```shell
curl "http://192.168.1.34:8080/adserver/www/delivery/api.php/rv_banners"
```

> The above command returns JSON structured like this:

```json
[
  {
    "bannerid": "1",
    "campaignid": "1",
    "contenttype": "gif",
    "pluginversion": "0",
    "storagetype": "web",
    "filename": "3473ec14ba94cb29be3729db693f4c82.gif",
    "imageurl": "",
    "htmltemplate": "",
    "htmlcache": "",
    "width": "320",
    "height": "240",
    "weight": "1",
    "seq": "0",
    "target": "",
    "url": "https://www.youtube.com/watch?v=-GlZvDxv9pA",
    "alt": "",
    "statustext": "",
    "bannertext": "",
    "description": "Finding Dory Banner",
    "adserver": "",
    "block": "0",
    "capping": "0",
    "session_capping": "0",
    "compiledlimitation": "",
    "acl_plugins": null,
    "append": "",
    "bannertype": "0",
    "alt_filename": "",
    "alt_imageurl": "",
    "alt_contenttype": "",
    "comments": "",
    "updated": "2016-07-06 10:33:44",
    "acls_updated": "0000-00-00 00:00:00",
    "keyword": "",
    "transparent": "0",
    "parameters": "N;",
    "status": "0",
    "ext_bannertype": null,
    "prepend": "",
    "iframe_friendly": "0"
  },
  {
    "bannerid": "2",
    "campaignid": "1",
    "contenttype": "",
    "pluginversion": "0",
    "storagetype": "html",
    "filename": "",
    "imageurl": "",
    "htmltemplate": "<A HREF=\"https://www.youtube.com/watch?v=-GlZvDxv9pAl\" onMouseOver=\"window.status='TEXT IN STATUS BAR'; return true\">\r\n<IMG SRC=\"http://blogs.coventry.ac.uk/uncovered/wp-content/uploads/sites/7/2016/01/Finding-Dory-GIF.gif\" BORDER=\"0\" WIDTH=\"468\" HEIGHT=\"270\" ALT=\"Come to my page!\"></A>",
    "htmlcache": "<a href=\"{clickurl}https%3A%2F%2Fwww.youtube.com%2Fwatch%3Fv%3D-GlZvDxv9pAl\" onMouseOver=\"window.status='TEXT IN STATUS BAR'; return true\"target=\"{target}\">\r\n<IMG SRC=\"http://blogs.coventry.ac.uk/uncovered/wp-content/uploads/sites/7/2016/01/Finding-Dory-GIF.gif\" BORDER=\"0\" WIDTH=\"468\" HEIGHT=\"270\" ALT=\"Come to my page!\"></A>",
    "width": "480",
    "height": "270",
    "weight": "1",
    "seq": "0",
    "target": "",
    "url": "",
    "alt": "",
    "statustext": "",
    "bannertext": "",
    "description": "HTML Banner",
    "adserver": "",
    "block": "0",
    "capping": "0",
    "session_capping": "0",
    "compiledlimitation": "",
    "acl_plugins": null,
    "append": "",
    "bannertype": "0",
    "alt_filename": "",
    "alt_imageurl": "",
    "alt_contenttype": "",
    "comments": "",
    "updated": "2016-07-06 08:52:23",
    "acls_updated": "0000-00-00 00:00:00",
    "keyword": "",
    "transparent": "0",
    "parameters": "N;",
    "status": "0",
    "ext_bannertype": "bannerTypeHtml:oxHtml:genericHtml",
    "prepend": "",
    "iframe_friendly": "1"
  }
]
```

This endpoint retrieves all banners.

### HTTP Request

`GET http://192.168.1.34:8080/adserver/www/delivery/api.php/rv_banners`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------


## Get a Specific banner

```shell
curl "http://192.168.1.34:8080/adserver/www/delivery/api.php/rv_banners/1"
```

> The above command returns JSON structured like this:

```json
{
  "bannerid": "1",
  "campaignid": "1",
  "contenttype": "gif",
  "pluginversion": "0",
  "storagetype": "web",
  "filename": "3473ec14ba94cb29be3729db693f4c82.gif",
  "imageurl": "",
  "htmltemplate": "",
  "htmlcache": "",
  "width": "320",
  "height": "240",
  "weight": "1",
  "seq": "0",
  "target": "",
  "url": "https://www.youtube.com/watch?v=-GlZvDxv9pA",
  "alt": "",
  "statustext": "",
  "bannertext": "",
  "description": "Finding Dory Banner",
  "adserver": "",
  "block": "0",
  "capping": "0",
  "session_capping": "0",
  "compiledlimitation": "",
  "acl_plugins": null,
  "append": "",
  "bannertype": "0",
  "alt_filename": "",
  "alt_imageurl": "",
  "alt_contenttype": "",
  "comments": "",
  "updated": "2016-07-06 10:33:44",
  "acls_updated": "0000-00-00 00:00:00",
  "keyword": "",
  "transparent": "0",
  "parameters": "N;",
  "status": "0",
  "ext_bannertype": null,
  "prepend": "",
  "iframe_friendly": "0"
}
```

This endpoint retrieves a specific banner.


### HTTP Request

`GET http://192.168.1.34:8080/adserver/www/delivery/api.php/rv_banners/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the banner to retrieve

