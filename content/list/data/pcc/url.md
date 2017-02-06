+++
date = "2016-08-01"
title = "URL (Data: campaign.pcc)"
original_url = "/list/data/pcc.html#url"
categories = [ "all-tag", "pcc-tag" ]
[menu.main]
    name = "URL (Data: campaign.pcc)"
    parent = "pcc"
+++

## Status

None

## Syntax

`URL:x|y|z`

## Parameters

-   x: Text (E-commerce site name. i.e. Amazon,
    DriveThruRPG, etc.)
-   x: WEBSITE
-   x: SURVEY
-   y: Text (Hypertext link)
-   z: Text (Link description)



<span id="url"></span> \*\*\* New 5.13.9

What it does
------------

-   Specifies the URL for hyper-links that will be displayed in the
    Source Tab in the Source Info panel when the dataset is selected.
-   Multiple HYPERLINK tags may be entered into the \*.pcc file.

Example
-------

> `URL:Barcommerce|http://www.barcommercesite.com/product_info.php?products_id=12345&affiliate_id=54321|Support PCGen by buying this source now!`
>
> Displays the text "Support PCGen by buying this source now!" as an
> active link to the URL
> "http://www.foobarcommercesite.com/product\_info.php?products\_id=12345&affiliate\_\\id=5432".
>
> `URL:WEBSITE|http://www.foopublisher.com|Visit FooPublishers website.`
>
> Displays the text "Visit Foopublishers website" as an active link to
> the website "http://www.foopublisher.com"
>
> `URL:SURVEY|http://www.pcgenubersite.com|Help PCGen out by visiting our user feedback page and letting us know what you think.`
>
> Displays the text "Help PCGen out by visiting our user feedback page
> and letting us know what you think!" as an active link to the website
> "http://www.pcgenubersite.com"

