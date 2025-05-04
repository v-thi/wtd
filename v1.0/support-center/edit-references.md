---
type: page
title: Edit References
listed: true
slug: edit-references
description: 
index_title: Edit References
hidden: 
keywords: 
tags: 
---

With %product%, you can seamlessly edit your OpenAPI 2/3 definitions using our intuitive visual API editor, which is powered by the robust Apicurio platform.

{% image url="https://uploads.developerhub.io/prod/8gDX/2hnau9qms7go14qziibemusc0cqe00l3f4cr6t30gwlx1ojqnj0shsb3j64kiatb.png" mode="responsive" height="1827" width="2920" %}
{% /image %}

## OpenAPI Editor Features

The OpenAPI Editor is a powerful and user-friendly web-based tool designed for creating and editing OpenAPI specifications. It fully supports versions 2.0, 3.0.0, 3.0.1, 3.0.2, and 3.0.3, with support for OpenAPI v3.1.0 and higher planned for the future. This intuitive editor simplifies the process of constructing your OpenAPI reference schema, allowing you to focus on development without requiring deep knowledge of the intricate details of the specification.

## Editing an API Definition

To edit an existing API definition, follow these steps:

- From the sidebar, choose Reference {% icon classes="fas fa-vector-square" /%}.
- Choose the API Reference to be edited from the list.
- Once the API Reference has fully loaded, locate and click on the Edit button situated in the bottom right corner of the screen. This action will open the API Editor in a new tab for your convenience.
- Make the necessary changes and then click on the "Save Draft" button to ensure that your updates are stored.

Once you are prepared to publish the API Reference, a publisher can simply click the Publish button located on the API Reference page.

## Create a new API Definition

To create a new API definition using our OpenAPI editor, please follow these steps:

- From the sidebar, choose Reference {% icon classes="fas fa-vector-square" /%}.
- Choose "Create new OpenAPI 3 reference". The API editor will launch in a new tab.

## Generators

Do you prefer to generate the OpenAPI file directly from your code to ensure it remains consistently aligned with your codebase? Explore the following options for generators that can create OpenAPI files from source code:

- Javascript: [swagger-jsdoc](https://www.npmjs.com/package/swagger-jsdoc)
- Express: [swagger-express](https://www.npmjs.com/package/swagger-express)
- PHP: [swagger-php](https://github.com/zircote/swagger-php)
- Symfony: [NelmioApiDocBundle](https://github.com/nelmio/NelmioApiDocBundle)
- Django: [django-rest-swagger](https://github.com/marcgibbons/django-rest-swagger)
- Flask: [flask-restplus](https://github.com/noirbizarre/flask-restplus)
- Ruby On Rails: [openapi-rails](https://github.com/slate-studio/openapi-rails)
- Go: [go-swagger](https://goswagger.io/)
- Spring: [springfox](https://github.com/springfox/springfox)

You can use our [API to upload API references automatically](/support-center/api-key#how-to-upload-references-programmatically).