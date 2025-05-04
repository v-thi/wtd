---
type: page
title: Intercom
listed: true
slug: intercom
description: 
index_title: Intercom
hidden: 
keywords: 
tags: 
---


Supercharged plan users can integrate %product% with Intercom to communicate with their users and to add a docs search widget in their messenger home.


{% image url="https://uploads.developerhub.io/prod/8gDX/cvmw2u007lnm7ab1i7opr9dr8qce8806auja2irskak4cg0jtjpf4m5lgpynt321.png" caption="" mode="300" height="1330" width="1500" %}
{% /image %}


## Setting up Intercom

- Click on Project Settings {% icon classes="fas fa-layer-group inv-icon" /%} in the sidebar to access Intercom settings under Integrations for Customers.
- Click Connect. You'll be taken through a flow to install %product% app on Intercom.


{% callout type="success" title="All set up!" %}
Intercom widget will now show on your published documentation.
{% /callout %}



{% image url="https://uploads.developerhub.io/prod/8gDX/6cxxaxdt5fenc7i78ak7v6x3y3a5bxpq4npn7xmy9al1l0xio7aarollmqw2ggoa.png" caption="" mode="600" height="1252" width="1970" %}
{% /image %}


## Adding Search Widget


{% callout type="warning" title="Installed Intercom before 12 Aug 2023?" %}
If you had installed Intercom on %product% before 12 Aug 2023, you need to [contact us](/support-center/contact-us) to add the search widget.
{% /callout %}



{% callout type="info" title="Only in Default Layout" %}
Intercom can only show widgets when using the default layout messenger, not the compact layout.
{% /callout %}


To add a %product% search widget to your messenger home, ensure that you first have [set up Intercom](/support-center/intercom#setting-up-intercom), then:

- From Intercom's platform, click on Messenger & Omnichannel in the sidebar.
- Under Messenger, click on Manage Settings.
- Under Customise Home with apps, click on Add an app.
- Choose %product%.
- Change the card title if needed.


{% image url="https://uploads.developerhub.io/prod/8gDX/6hitr7qm2mlg52iv1n7wy9jjigknypa3pfpd09erp3plky0cwsxoyuk0305bk8ou.png" caption="" mode="300" height="1700" width="1124" %}
{% /image %}


## Changing Intercom Region or Settings

To apply your own `intercomSettings`, including if you wish to change the data region, then you can do so using [auto$](/support-center/custom-javascript). Add a script tag that assigns the `intercomSettings` needed, such as:


{% code %}
{% tab language="json" %}
<script>
  window.intercomSettings = {
    api_base: "https://api-iam.eu.intercom.io"
  };
</script>
{% /tab %}
{% /code %}


