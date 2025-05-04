---
type: page
title: Private Documentation
listed: true
slug: password-protection
description: 
index_title: Private Documentation
hidden: 
keywords: visitor auth, visitor authentication, guest authentication, guest auth
tags: 
---


Supercharged plans admins can set their documentation portal as private, disallowing everyone on the internet to be able to access it. The protected project can be viewed by:

- Visiting the documentation site, and entering a [shared password](/support-center/password-protection#password-protect-set-up).
- Opening a [shared link](/support-center/password-protection#link-sharing).
- Invited readers through [magic links](/support-center/email-invite).
- [Custom login](/support-center/custom-login) flow using JSON Web Tokens (JWT).

If you are on an enterprise plan, then we also provide reader authentication through your intranet.

## Comparison Between Different Methods


{% table %}
| Method | Security Level | Ease of Access | Needs a Developer? | Usage | 
| ---- | ---- | ---- | ---- | ---- | 
| [Password](/support-center/password-protection#password-protect-set-up) | Weak. Your readers might leak the password. | Need to remember a password | No | Use to block out competitors and crawlers. | 
| [Shared Link](/support-center/password-protection#link-sharing) | Weak. Your readers might leak the link. | Easy, click on a link. | No | Use to block out competitors and crawlers. | 
| [Reader Magic Link](/support-center/email-invite) | Strong | Easy, readers goes to the docs site, requests a magic link and opens the link. | No | Use to secure data and control access. | 
| [Custom Login](/support-center/custom-login) | Strong | Easy, reader needs to go to the docs site, but might need to log into your own site. | Yes | Use to secure data, control access and [personalise](/support-center/personalised-docs) docs. | 
| Intranet (Enterprise only) | Strong | Easy, reader just needs to go to the docs site. | Yes | Use to secure data and control access. | 
{% /table %}

## Password Protect Set up

To set up password protection:

- Go to your Project Settings {% icon classes="fas fa-layer-group inv-icon" /%} from the sidebar.
- Click on Make Private (or Manage Access).


{% image url="https://uploads.developerhub.io/prod/8gDX/36r7557zmvuk41bsn5fllmhhcpn9x4tmskcziiduf7fpj0j75tjqqt3dzltsyzgx.png" caption="" mode="set" height="451.3125" width="448" %}
{% /image %}


- Choose Password.
- Input the password.
- Click on Save.


{% image url="https://uploads.developerhub.io/prod/8gDX/ifxphy74ecad6jdken0h03t3sa5vnzpni9i7m57fipc7me7hf2hn6ziwsvgwcbkt.png" caption="" mode="responsive" height="1088" width="1424" %}
{% /image %}



{% callout type="success" title="Success" %}
Great, all the published pages of this project are now protected by a password
{% /callout %}


To try it out, go to the live mode of your documentation. You will be presented with such a page.


{% image url="https://uploads.developerhub.io/prod/8gDX/n8snlrzeprxm4gd5un6m0qqf92gmw2offjfrhx7w9ok40tyz7iofmgshn22tvhrb.jpg" caption="" mode="responsive" height="1698" width="2276" %}
{% /image %}


Once a reader inputs the right password, they will continue to be logged in for 24 hours.


{% callout type="warning" title="Warning" %}
You should not save confidential or sensitive information in a password protected project. This is to prevent the general public and search engines from accessing your pages rather than to secure data.
{% /callout %}


## Link Sharing

Once a project is protected by a password, you can share a link which accesses the project without the need to enter a password. You can use this feature to provide only your customers with read access by sharing this link internally with them.

To share a link:

- Open Project Settings {% icon classes="fas fa-layer-group inv-icon" /%}
- Next to Manage Access, click on Share Link {% icon classes="fas fa-share-alt" /%} icon.


{% image url="https://uploads.developerhub.io/prod/8gDX/5l7l3lkzoxgrfbskdwm5ul7jf4dletsxxrknn44zato4f5uq1r1k21i6ssyzqohd.png" caption="" mode="set" height="467.34375" width="478" %}
{% /image %}


- You can send invitations directly to your readers. Separate e-mail address by using commas.
- Or you can copy the link and paste it.


{% callout type="warning" title="Warning" %}
The link will be revoked once the password changes or is removed.
{% /callout %}


## Using Login URL

If your docs are protected by using a [shared link](/support-center/password-protection#link-sharing) or a [custom login flow](/support-center/custom-login), then your readers probably need to authenticate with your own website first, and you need to provide them with a URL that allows them to authenticate on your docs. Thus, we can make this easier by redirecting your unauthenticated readers to a URL which you specify, where:

- If you are using secure link sharing, it would take them to the page where they can find the link, or the page that redirects them to the link if they're authenticated on your own website.
- If you are using [custom login](/support-center/custom-login), it would take them to an authentication page which if they are already logged in to your own website, then it just redirects back with a valid URL to the docs site, otherwise would prompt them to log in first.

To setup login URL:

- Go to Project Settings {% icon classes="fas fa-layer-group inv-icon" /%} in the sidebar.
- Click on Manage Access.
- Under Login URL, input the URL. An example would be `https://pied-piper.com/docs-login`.

### Disabling Protection

To disable password protection:

- Go to Project Settings {% icon classes="fas fa-layer-group inv-icon" /%} in the sidebar.
- Click on Manage Access.
- Choose Public {% icon classes="fas fa-unlock" /%}

Immediately, the project will be unprotected.


{% callout type="warning" title="Warning" %}
All your published versions will continue to be published. Make sure to unpublish any version that you do not want accessible to the general public before you unprotect the project if needed.
{% /callout %}


