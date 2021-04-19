---
description: Section incomplete
---

# Tag Deployment

## **How to avoid tag aliasing**

Aliasing can occur when multiple tags emit a signal at the same time. Sometimes these interacting signals can produce a pattern which match a different tag that is not actually present. This is due to the nature of how the unique tag ID is encoded in the signal. However, the parameters used to define these IDs are quite stringent, making aliasing only an issue in specific conditions.

#### _Strategic tag deployment_

To help mitigate aliasing, we recommend keeping numbers low at any given tagging site. This can be done by staggering deployments, either spatially or temporally. Most aliasing is caused by tags which have the same burst interval but a different Lotek ID. That means if you have more than one burst interval in your selection of tags, you can deploy more tags at any given site with a reduced risk of aliasing. However, do not deploy more than one tag with the same Lotek ID, even if they have different burst intervals!

\*\*\*\*[**Read more about how to avoid tag aliasing.**](tag-aliasing.md#how-to-avoid-tag-aliasing-1)  




