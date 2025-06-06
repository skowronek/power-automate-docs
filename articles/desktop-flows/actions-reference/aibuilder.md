---
title: AI Builder actions reference
description: Learn about the available AI Builder action.
author: Mattp123
ms.service: power-automate
ms.subservice: desktop-flow
ms.topic: reference
ms.date: 10/19/2023
ms.author: matp
ms.reviewer: cochamos
contributors:
  - jpapadimitriou
search.audienceType: 
  - flowmaker
  - enduser
---

# AI Builder actions (preview)

[!INCLUDE [cc-beta-prerelease-disclaimer](includes/cc-beta-prerelease-disclaimer.md)]

The AI Builder group contains the **Create text with GPT (preview)** action that creates text using the GPT language model.

> [!IMPORTANT]
> - This is a preview feature.
> - Preview features aren’t meant for production use and may have restricted functionality.
> - These features are available before an official release so that customers can get early access and provide feedback.
>
> Further strengthening our commitment to [responsible AI](https://www.microsoft.com/en-us/ai/responsible-ai) we're introducing some updates related to the utilization of **Create text with GPT (preview)** action in the Power Automate for desktop October 2023 update.
> Specifically: 
> - A **Display input dialog** action or **Display message** action must accompany each use of the **Create text with GPT** action
> - The **Display input dialog** action or **Display message** action must contain the response from the **Create text with GPT** action in its body so it is clearly presented to the user
>
> Make sure that flows that utilize the **Create text with GPT (preview)** action check those two points. If either of those steps is omitted, the respective flow(s) will result in an error.
>
> Also note the following:
> - This capability is in process of rolling out, and may not be available in your region yet.
> - This capability may be subject to usage limits or capacity throttling.
> - The GPT model might make mistakes or have biases and other undesirable content. Therefore, to ensure that the AI-generated content is accurate, appropriate, and free from bias, always have humans review it.
> - This capability is under gated access. Apply for consideration to take part in the trial. To apply, go to [Limited preview request](https://forms.office.com/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR2LogRPRiTJDo1Rd8KnmcFRUMzlLTDZVQlJKSzNIWkVCMzE0VDFYVzk2QS4u).

After deploying the action, select **Create instructions** to open the instructions wizard. The wizard allows you to create instructions using existing templates or start from blank.

Learn more about the Text generation model (preview) in [the Text generation model overview (preview)](/ai-builder/prebuilt-azure-openai).

:::image type="content" source="media/aibuilder/create-text-with-gpt.png" alt-text="Screenshot of the Create instructions button in the Create text with GPT action.":::

>[!IMPORTANT]
>It's mandatory that you add either a **Display input dialog** or **Display message** action and pass either of the generated outputs of the **Create text with GPT (preview)** action (**PredictV2Response**, **PredictV2TextResponse**) in its body. This will require a human review of the generated messages.  If either of those steps is omitted, the respective flow(s) will result in an error.

Example approach: Add a Display message action with Yes - No buttons to require a human review of the generated content. An error appears when this action doesn't exist. Learn more about the Display message action in [Message boxes actions](display.md).

:::image type="content" source="media/aibuilder/display-message.png" alt-text="Screenshot of the Display message action that prompts users to review the generated content.":::

## <a name="callgpt"></a> Create text with GPT (preview)

Get a response generated by GPT.

### Input parameters

|Argument|Optional|Accepts|Default Value|Description|
|-----|-----|-----|-----|-----|
|Instructions|No|[Text value](../variable-data-types.md#text-value)||Provide instructions for the GPT model to perform a task|

### Variables produced

|Argument|Type|Description|
|-----|-----|-----|
|PredictV2Response|[Connector object](../variable-data-types.md#connector-object)||
|PredictV2TextResponse|[Text](../variable-data-types.md#text-value)||

### <a name="callgpt_onerror"></a> Exceptions

|Exception|Description|
|-----|-----|
|Endpoint failure|Indicates an endpoint failure|
