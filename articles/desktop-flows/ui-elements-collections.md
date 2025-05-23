---
title: UI elements collections
description: Learn about UI elements collections in Power Automate desktop flows.
author: yiannismavridis
ms.service: power-automate
ms.subservice: desktop-flow
ms.topic: article
ms.date: 03/12/2025
ms.author: iomavrid
ms.reviewer: dmartens
contributors:
  - yiannismavridis
  - DanaMartens
search.audienceType: 
  - flowmaker
  - enduser
---

# UI elements collections in desktop flows

UI elements collections that organization users develop and publish to the respective environments can be included in desktop flows.

In Power Automate for desktop, UI elements are elements that are grabbed and captured from the various user interfaces (either desktop applications or web pages). These elements can be text fields, buttons, links, or anything else that you can interact with in the target applications.

After these elements are captured, they can be associated with the respective UI or web automation actions, so that the corresponding interaction with the elements can be automated in the context of desktop flows.

Previously, UI elements were only available separately to each desktop flow. This means that they needed to be captured individually in the context of each desktop flow built, even if the elements happened to be exactly the same among multiple desktop flows. To avoid this, UI elements collections now offer makers and admins the ability to have control and central management over "groups" of UI elements, which can be shared across multiple users and imported in multiple desktop flows as reusable components. In this way, in case of an application update for instance, the UI elements collection only needs a one-time adjustment - all desktop flows referencing this collection in the same environment should then reflect that change automatically.

> [!NOTE]
> - UI elements collections exist at the environment level and are stored in the **Desktop Flow Module** Dataverse table. As a best practice, use a "dev—test—prod" model when deploying UI elements collections.
> - To add a UI elements collection to a solution, go to your solution and then select **Add existing** > **More** > **Other** > **Desktop Flow Module** > ***your_collection***. This action adds the collection and all its dependencies.
> - If your solution contains a desktop flow that references a UI elements collection, select the desktop flow and then select **Advanced** > **Add required objects** to add all dependent components, including the UI elements collection and its dependencies, to the Solution.

## Prerequisites

- Power Automate for desktop 2.43 or later.
- This feature requires an environment where the [Power Automate v2 schema](schema.md) is enabled. In v1 schema environments, UI elements collections aren't available.
- An Attended RPA license is required to include and use UI elements collections in desktop flows, given that access to the flow designer of Power Automate for desktop is needed.
- If you use custom security roles to manage access, Power Platform admins need to update the role to include read permission for the Desktop Flow Module table (`prvReaddesktopflowmodule`).

## Known limitations

- Upload date might differ in the portal than what is shown in the Assets library inside Power Automate for desktop.

## Next steps

[Create and publish UI elements collections](create-ui-elements-collections.md)

## Related information

- [Assets library](assets-library.md)
- [Manage UI elements collections](manage-ui-elements-collections.md)
- [Use and update UI elements collections](use-update-ui-elements-collections.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
