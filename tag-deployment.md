---
description: Section incomplete
---

# Tag Deployment

## **How to avoid tag aliasing**

Aliasing is caused by multiple tags emitting a signal at the same time and overlapping. Sometimes these interacting signals can produce a pattern which matches a different tag that is not actually present. This is due to the nature of how the unique ID is encoded in the signal. However, the parameters used to define these IDs are quite stringent, making aliasing an issue only in specific conditions.

#### _Strategic tag deployment_

To help mitigate aliasing, we recommend keeping numbers low at any given tagging site. This can be done by staggering deployments, either spatially or temporally. Most aliasing is caused by tags which have the same burst rate but a different Lotek ID. That means if you have more than one burst rate in your selection of tags, you can deploy more tags at any given site with a reduced risk of aliasing. However, do not deploy more than one tag with the same Lotek ID, even if they have different burst rates!

\*\*\*\*[**Read more about how to avoid tag aliasing.**](tag-aliasing.md#how-to-avoid-tag-aliasing-1)  




