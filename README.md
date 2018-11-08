# OrchestraCMS Lightning Components Developer Reference

<!-- MarkdownTOC depth=3 -->

1. [Summary](#summary)
    1. [Compatibility](#compatibility)
    2. [Prerequisites](#prerequisites)
    3. [Deployment](#deployment)
    4. [Configuration](#configuration)
2. [Examples](#examples)
    1. [Custom Content Templates](#templates)
    2. [Changing Component Markup](#markup)
    3. [Extending Components](#extending)
    4. [Override & Enhancer Controllers](#controllers)
3. [Versioning](#versioning)
    1. [Major Versions](#major-versions)
    2. [Minor Versions](#minor-versions)
    3. [Patch Versions](#patch-versions)

<!-- /MarkdownTOC -->

<a name="summary"></a>
## Summary

This repository contains examples of developing with OrchestraCMS's Lightning Components. It includes
example content types and templates, as well as lightning components for extending and overriding the
functionality provided by OrchestraCMS.

Please see the official documentation on [Stantive Technologies Group's Developer Site](https://developer.stantive.com/) 
for information on how to use this example code.

<a name="compatibility"></a>
### Compatibility

This code requires a minimum of OrchestraCMS package 8.216 (November 2018, v10.0 Build #8.216).

<a name="prerequisites"></a>
### Prerequisites

1. A compatible version of OrchestraCMS is installed in the target Salesforce organization.
2. OrchestraCMS API Resources deployed to your org
3. A Community using a lightning template (like Customer Service)
4. A site has been created in OrchestraCMS.

<a name="deployment"></a>
### Deployment

1. Deploy the following Lightning Components to the target Salesforce organization
    1. SampleAccordionBody
    2. SampleAccordionTemplate
    3. SampleArticleDetail_Template
    4. SampleArticleEditor
    5. SampleArticleSummaryCompact_Template
    6. SampleArticleSummary_Template
    7. SampleContentLoaderBody
    8. SampleContentLoaderSlider
    9. SampleLoadingSpinner
    10. SampleProductDetail
    11. SampleProductSummary
    12. SampleTaxonomyMenuBody
    13. SampleTaxonomyMenuItem 
2. Deploy the following Apex classes to the target Salesforce organization
    1. SampleProductEnhancerController.cls
    2. SampleProductOverrideController.cls
3. Deploy the following Static Resources to the target Salesforce organization
    1. CTCArticleSummaryResource.resource
    2. SampleOverrideCSS.resource

<a href="https://githubsfdeploy.herokuapp.com">
  <img alt="Deploy to Salesforce"
       src="https://raw.githubusercontent.com/afawcett/githubsfdeploy/master/deploy.png">
</a>

<a name="configuration"></a>
### Configuration

Create OrchestraCMS Content Layout records by importing `CTCExport.txt` from the Content Templates
page within the target OrchestraCMS site's setup menu.

Create the following content type(s) and add content templates as indicated.

```
Name: Article
Label: Article
Templates:
    Article Compact, autocreate
    Article Detai, autocreate, default
    Article Summary, autocreate
    CTC Article Summary, autocreate
```

```
Name: FAQ
Label: FAQ
Templates:
    Accordion Section, autocreate, default
```

```
Name: Product
Label: Product
Templates:
    Sample Product Detail, autocreate, default
    Sample Product Summary, autocreate
```

<a name="examples"></a>
## Examples

<a name="templates"></a>
### Custom Content Templates

Three "Article" content templates are provided. Demonstrates how to link from a summary template to 
a detail template, and how to use default components for like tracking and chatter. A fourth template
is provided as an example of using the "Markup" field in Content Template Creator

#### Metadata
- SampleArticleDetail_Template
- SampleArticleSummary_Template
- SampleArticleSummaryCompact_Template
- SampleArticleEditor
- CTCArticleSummaryResource.resource 

<a name="markup"></a>
### Changing Component Markup

Examples of overriding component markup for Static Content, Dynamic Content, Taxonomy Menus, and any 
component's loading spinner.

#### Metadata
- SampleAccordionBody
- SampleAccordionTemplate
- SampleContentLoaderBody
- SampleLoadingSpinner
- SampleTaxonomyMenuBody
- SampleTaxonomyMenuItem

<a name="extending"></a>
### Extending Component Functionality

An example of extending a Content Loader component to act as a slideshow/carousel

#### Metadata
- SampleContentLoaderSlider

<a name="controllers"></a>
### Override & Enhancer Controllers

Examples of replacing server-side functionality, and returning extra information along with content

#### Metadata
- SampleProductDetail
- SampleProductSummary
- SampleProductEnhancerController.cls
- SampleProductOverrideController.cls

<a name="versioning"></a>
## Versioning

Versions of this content type are numbered MAJOR.MINOR.PATCH.

Any modifications to this code outside of this repository are customizations and will impact upgradeability.

<a name="major-versions"></a>
### Major Versions

Major versions introduce new functionality and may break existing implementations.

<a name="minor-versions"></a>
### Minor Versions

Minor versions introduce new functionality, but will not break existing implementations.

<a name="patch-versions"></a>
### Patch Versions

Patches correct defects in the implementation and do not introduce new functionality.