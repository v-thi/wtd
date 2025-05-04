---
type: page
title: Custom CSS
listed: true
slug: custom-css
description: Apply project-wide CSS changes and have complete design control using Custom CSS. Learn how to customize CSS, test it, revert changes, and more.
index_title: Custom CSS
hidden: 
keywords: 
tags: 
---

{% html %}
<div class="grow-border text-left">
<div class="grow-star">⭐</div>
    Available in Grow Projects
</div>
{% /html %}

Apply project-wide CSS changes and enable complete design control using Custom CSS.

{% callout type="info" title="Need to be more specific?" %}
If you wish to apply (or test) on a version, then you can use the selector `.customise .version-{{versionSlug}}`.
{% /callout %}

## Customizing CSS

To customize CSS:

- Open Project Settings {% icon classes="fas fa-layer-group inv-icon" /%} from the Sidebar.
- Under Customize, select Edit CSS.
- Enter the custom CSS, and click Save. This will save the CSS in draft mode, so you can test it out.
- To publish it to readers, click Save & Publish.
- To revert the draft changes, click Revert.

The CSS will be applied instantly, ensuring that your changes take effect without delay.

## Testing CSS

To ensure your CSS modifications are functioning as intended before delivering them to your customers, it's important to test your changes thoroughly. To begin testing your CSS, simply click on the Save button located in the Custom CSS window. At this point, the updated CSS will take effect immediately within the editor, allowing you to see the results in real time. Additionally, if you utilize any of the Go To buttons available in the sidebar, you will also be able to observe your CSS changes reflected in the published documents. This enables a comprehensive review of your styles prior to final deployment.

If you want to double check what your readers see after you click the Go To button, then open the published docs in an incognito window of your browser.

You can revert the changes from the Custom CSS window.

{% callout type="warning" title="Reverting Draft CSS" %}
When you revert the CSS, the draft changes are discarded and lost.
{% /callout %}

{% callout type="info" title="Testing while frontend application is pinned" %}
To test latest frontend application on the readers site if your [frontend application is pinned](/support-center/custom-css#pinning-frontend-application-version), add `?deployment_id=latest` to the URL. To confirm which application version is being used, check the `X-DeveloperHub-Version` header in the first network request.
{% /callout %}

## Testing Dark Theme

To test the dark theme without enabling it for your readers, utilize the [Change Theme](/support-center/developer-tools#change-theme) function. This approach allows you to apply the dark theme temporarily without altering the project settings, ensuring that your audience remains unaffected during the testing process.

## Disabling Styles

To determine if a style applied through Custom CSS is causing any issues, you can temporarily disable all custom styles for your browser. Simply append the query `?disableStyles=true` to the URL of any published document. This allows you to see how the document renders without the influence of custom styles, helping you identify any potential problems.

If your docs are at `[https://example.com/docs](https://example.com/docs)`, you can turn off custom styles for your session by using `[https://example.com/docs?disableStyles=true](https://example.com/docs?disableStyles=true)`.

After refreshing the page without using `disableStyles=true`, your custom styles will be reactivated automatically.

## Why customize CSS?

By customizing CSS, you can:

- Apply an image to the navigation header.
- Change the index style.
- Add icons to categories in the index, or apply a smooth colour transform like in our docs.
- Animate buttons.
- Import another CSS file using `@import url(...)` .
- Use your own [custom (non Google Font) font](https://developerhub.io/blog/using-your-own-font/).
- Create a custom landing page, removing sidebars and titles.
- Change the [code theme](/support-center/code-theme).
- Or anything you can think of, really...

{% callout type="warning" title="Warning" %}
The CSS is not encapsulated, meaning it applies globally across the application. Since the %product% CSS changes frequently, we cannot guarantee a consistent design; for more details, please refer to our guide on [Pinning Frontend Application Version](/support-center/custom-css#pinning-frontend-application-version). To ensure your styles are applied as intended, you may want to consider adding `!important` to your CSS declarations.
{% /callout %}

## CSS Best Practices

%product% CSS is not encapsulated and applies globally. This means that you can change everything - including what you see in the editor, including the editor itself! With this amount of great power, comes great responsibility, so make sure you follow these best practices. The examples will work through one case: "How to change the colour of the page title".

{% callout type="warning" title="Ensure Cross-Platform Compatibility" %}
Make certain that any Custom CSS modifications are compatible with all display sizes and input devices. The default CSS is crafted to function seamlessly across phones, tablets, laptop screens, and larger displays. **It is essential to rigorously test the CSS changes you implement on all screen sizes to guarantee a satisfactory experience for readers.**
{% /callout %}

### {% badge type="custom" text="1" /%} Use `.customise`

`.customise` is a CSS selector that you should use for all your CSS rules. It includes everything that the editor does not, which is what you may want to customize. For example:

{% code %}
{% tab language="css" %}
/* DON'T DO THIS ❌ - Will change all heading 1 everywhere, in editor, in dashboard... horrible */
h1 {
  color: green !important;
}

/* PREFER TO DO THIS - Will change all heading 1 only where it is expected to be changed */
.customise h1 {
  color: green !important;
}
{% /tab %}
{% /code %}

### {% badge type="custom" text="2" /%} Use `.live`

`.live` is a CSS selector that you should use in your CSS rules. It ensures that the CSS only loads on your live docs site and not in the editor. If you change the page styles in the editor, it may cause inconsistencies and break features if the CSS isn't written carefully. Therefore, it's best to have these styles apply only on the live docs site. For example:

{% code %}
{% tab language="css" %}
/* DON'T DO THIS ❌ - Will change all heading 1 only in live docs site and editor */
.customise h1 {
  color: green !important;
}

/* PREFER TO DO THIS - Will change all heading 1 only in the live docs site */
.customise.live h1 {
  color: green !important;
}
{% /tab %}
{% /code %}

### {% badge type="custom" text="3" /%} Use specific selectors

In our previous examples, `h1` serves as a rather broad selector. To effectively modify the page title color, it is advisable to use a more specific selector, particularly within the context of Documentation. This approach ensures precise targeting and avoids unintended style changes to other elements.

{% code %}
{% tab language="css" %}
/* DON'T DO THIS ❌ - Will change all heading 1 only in live docs site */
.customise.live h1 {
  color: green !important;
}

/* DO THIS INSTEAD ✅ - Will change the page title only in Documentation in the live docs site */
.customise.live .documentation .title-container>.title {
  color: green !important;
}
{% /tab %}
{% /code %}

{% callout type="error" title="Do Not Change Generic Styles" %}
Changing the CSS of generic selectors like `table`, `p`, `.container`, `.row`, `img`, etc. will alter the overall appearance and may disrupt the editor and live view functionality. We use Bootstrap extensively, so altering its default styles is not advised. Instead, choose a specific selector to apply your styles.

If you're making a landing page, create specific selectors. For instance, if you want to use a `.container`, also add a `.x-container` selector to it and apply styles to `.x-container` instead of the general `.container`.
{% /callout %}

## CSS Customization Examples

See [auto$](/support-center/css-customisations).

## Examples on Page

As we are committed to preserving the style of our documentation, which we deeply appreciate, we will present some styled items in this section.

- Sign up now button with hover effect.

{% html %}
<div class="text-left">
<a class="doc-button" href="https://app.developerhub.io/signup" target="_blank">Sign up now 🚀</a>
</div>
{% /html %}

- Links to other documentations.

{% html %}
<div class="row">

	<div class="col text-left px-2 py-3 mx-3 doc-lg-button">

		<a href="https://docs.developerhub.io" _target="blank">

			<i class="fas fa-book fa-2x ml-2 mr-2"></i>

			<div class="d-inline" style="font-size: 1.3em; color: var(--font-color)">Documentation</div>

		</a>

	</div>

	<div class="col text-left px-2 py-3 mx-3 doc-lg-button">

		<a href="https://swagger.developerhub.io" _target="blank">

			<i class="fas fa-vector-square fa-2x ml-2 mr-2"></i>

			<div class="d-inline" style="font-size: 1.3em; color: var(--font-color)">Reference</div>

		</a>

	</div>

</div>
{% /html %}

- Sign up forms.

{% html %}
<div class="container pt-3 pb-5" style="background: hsl(33, 100%, 98%); border-radius: 12px">

	<div class="row">

		<div class="col text-center">

			<div class="mt-2" style="font-size: 1.5em; color: #333">Sign up for our updates</div>

			<p style="color: #333">We'll send you updates every week</p>

		</div>

	</div>

	<div class="row">

		<div class="col text-center">

			<input type="text" class="d-inline-block doc-input"/><button class="doc-button" onclick="alert('Gotcha');">Sign up</button>

		</div>

	</div>

</div>
{% /html %}

## CSS Variables

We have created configurable variables that allow you to easily adjust the look and feel of your interface. When you set [theme](/support-center/theme), these variables will be automatically updated to reflect your changes.

{% code %}
{% tab language="css" %}
:root {
  --brand: #5368e7; /* Your brand color - auto assigned from project */
  --brand-transparent: #5368e754; /* Your brand color with transparency - auto assigned from project */
  --reference-hue: 230; /* Your brand color's hue - used in reference right column */
  --font: Nunito, "SansSerif"; /* Your font - auto assigned from project */
  --font-size: 15px; /* Font size for page content */
  --secondary-font-size: 16px; /* Font size for index content */
  --link: #ff536b; /* Your link color - auto assigned from project */
  --inline-code: #444444; /* Your inline code color */
  --inline-code-bg: #f5f7f7; /* Your inline code background color */
  --nav-link: #FFFFFF; /* Your navigation link color - auto generated from brand and link colour */
  --dominant: #5368e7; /* Your dominant colour - auto generated from brand and link colour */
  --code-font: Roboto Mono,Consolas,Monaco,Andale Mono,Ubuntu Mono,monospace; /* Font used for code blocks */
  --code-font-size: 13px; /* Size of font used for code blocks */
  
  --bg-color: #FFF; /* Background color */
  --alt-bg-color: #FFF;  /* Used in some controls for differentiating from background color in dark mode */
  --font-color: #333; /* Font color */
  --heading-color: #444; /* Heading color */
  --category-color: #555; /* Category (in index) color */
  --toc-link-color: #666;  /* TOC text color */
  --table-second-color: #FAFAFA;  /* Alternating table background color */
  --page-border-color: #F1F1F1;  /* Left and bottom page border color */
  
  --index-width: calc(var(--secondary-font-size) * 18); /* Width of documentation index */
  --reference-index-width: calc(var(--secondary-font-size) * 16); /* Width of reference index */
}
{% /tab %}
{% /code %}

To modify the variables used when dark theme is enabled, use the selector `.dark-mode`, for example:

{% code %}
{% tab language="css" %}
.dark-mode {
  --brand: #123456;
  --link: blue;
}
{% /tab %}
{% /code %}

### Font Weights

If your assigned font does not have all the weights we use on %product% then you can reassign some weights to another:

{% code %}
{% tab language="css" %}
:root {
  --fw-100: 100;
  --fw-200: 200;
  --fw-300: 300;
  --fw-400: 400;
  --fw-500: 500;
  --fw-600: 600;
  --fw-700: 700;
  --fw-800: 800;
  --fw-900: 900;
}
{% /tab %}
{% /code %}

For example, if weight 500 does not exist, then you may set `--fw-500: 600`, so font weight 600 is used whenever 500 is expected.

{% callout type="warning" title="Other variables" %}
We have more variables which are not mentioned here, such as `--shadeX` and `--helperX` which are not built to be modified by the user. Changing them will definitely lead to unexpected results.
{% /callout %}

## Pinning Frontend Application Version

As we continue to enhance the features of %product%, we may update the DOM, CSS, and JavaScript components that contribute to your documentation site. It's important to note that these updates could potentially impact your custom CSS modifications, especially if you have implemented significant changes. Consequently, this may result in unexpected alterations to the site's appearance.

To prevent unexpected changes from impacting your users, you have the option to pin the frontend application version to a specific deployment. This ensures that any modifications made to the single-page application will not be visible to your readers until you decide to update it. Additionally, we may automatically pin your frontend application version during significant updates that could potentially affect any custom CSS modifications you have implemented.

To pin your frontend application version:

- From the left sidebar, click on Project Settings {% icon classes="fas fa-layer-group inv-icon" /%}.
- Under Advanced Settings, click the button next to Pin frontend application version.
- Choose a version according to its date and description.

To unpin the frontend application version, choose Latest version.

Change might take up to 5 minutes to reflect on the docs site. The change only reflects on the readers site, not in the editor.

{% callout type="warning" title="Important" %}
This stops all updates to your docs site and ensures your reader doesn't see unexpected styles. **You should change the custom CSS as soon as you can and switch back to the Latest version.** We can't promise that older versions will keep working.
{% /callout %}

## Migrating to Latest Frontend Application Version

If you are using an older version of the application and want to update to the latest version for new features, follow these steps:

1. **Test how the docs would look with latest frontend application version**

To test the latest frontend application on the readers site, if your application is pinned, add `?deployment_id=latest` to the URL. To check which version is being used, look at the `X-DeveloperHub-Version header` in the first network request.

Load at least the landing page, documentation page, and API reference with `?deployment_id=latest` appended to the end of the URLs. Assess whether the pages appear as intended. If any discrepancies are found, adjust the CSS/JS in [draft mode](/support-center/custom-css#testing-css) and continue refining until the pages look flawless.

{% callout type="info" title="?deployment_id=latest is temporary" %}
Make sure that everytime you reload the page and wish to see it in latest application version, you add `?deployment_id=latest`.
{% /callout %}

2. **Publish CSS/JS changes**

Now that your CSS and JavaScript changes are finalized and flawless, it is time to share them with your audience. Publish these updates for your readers to enjoy!

3. **Unpin frontend application version**

To unpin your frontend application version:

- From the left sidebar, click on Project Settings {% icon classes="fas fa-layer-group inv-icon" /%}.
- Under Advanced Settings, click the button next to Pin frontend application version.
- Choose "Latest".