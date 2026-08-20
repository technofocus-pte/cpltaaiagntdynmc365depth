---
lab:
title: Design Emails with Copilot in Customer Insights – Journeys

description: Learn how to use Copilot in Dynamics 365 Customer Insights – Journeys to generate email content ideas, apply AI-assisted themes and branding, and prepare marketing emails for delivery.

duration: 30 mins

level: 200

islab: True

primarytopics: Dynamics 365 Customer Insights- Journey
---

# Design and style emails with AI-assisted themes using Copilot in Customer Insights – Journeys

## Scenario

You are a Marketing Specialist at Contoso Retail, responsible for creating engaging email campaigns for customers. To accelerate campaign creation and maintain consistent branding, you will use Microsoft Copilot in Dynamics 365 Customer Insights – Journeys. By leveraging AI-generated content ideas and theme customization tools, you will design a professional marketing email, apply branding elements, and validate the email before preparing it for delivery.

## Objective: 

In this lab, you will learn how to design and style marketing emails using Copilot in Customer Insights – Journeys. You will learn how to enable Copilot features, use AI-generated content ideas to accelerate email creation, and apply theme customization tools to build branded email designs. You will also learn how to configure compliance elements, preview emails, and perform test sends to validate email styling and content before publishing.

## Overview
Dynamics 365 Customer Insights – Journeys includes Copilot capabilities that help marketers create compelling email campaigns more efficiently. In this lab, you will first enable Copilot features within the Customer Insights – Journeys environment. You will then create a new email and use Copilot to generate content ideas based on business scenarios and suggested topics. After generating content, you will use the Theme assistant to apply branding, colors, and styling to create a consistent visual experience. Finally, you will configure sender and compliance information, preview the email, perform a test send, and prepare the email for distribution.

## Lab Prerequisites
Before starting this lab, ensure that you have:

- Access to a Dynamics 365 Customer Insights – Journeys environment.

- A Microsoft 365 or Dynamics 365 account with appropriate permissions.

- Access to the Power Platform Admin Center.

- A configured Customer Insights – Journeys environment with a default brand profile and sender profile.

- A valid email address for performing test sends.

- Basic familiarity with email marketing concepts and Dynamics 365 Customer Insights – Journeys.


## **Task 1: Enable Copilot in Customer Insights – Journeys**

1. Go to **Power Platform admin center** by navigating to **+++https://admin.powerplatform.microsoft.com+++** and if required, sign in using your given **Office 365 admin tenant** credentials.

2. From the left navigation pane, select **Manage** > **Environment** and then click on **Marketing trial**.

  ![](./media/image1.png)

3. Click on **Environment URL**.

  ![](./media/image2.png)

4. Select **Customer Insights – Journeys**.

  ![](./media/image3.png)

5. Select **Customer Insights – Journeys** if asked.

  ![](./media/image4.png)

6. You will be on the **Customer Insights – Journeys** portal.

  ![](./media/image5.png)

7. Go to the **Change** area, select **Settings.**

  ![](./media/image6.png)

8. From left navigation pane, select **Settings**. Under **Overview**, select **Feature switches**.

  ![](./media/image7.png)

9. Scroll down and under the **Copilot** section, enable the **Global opt-in consent** toggle and **Global data sharing consent** toggle. Select **Save** in the top-right corner.

  ![](./media/image8.png)

10. Select **Ok**.

  ![](./media/image9.png)

## Task 2: Generate content ideas using Copilot

1. Select **Real-time journeys** from the Change area.

   ![](./media/image10.png)

2. From the left navigation pane, select **Emails** under **Channels**.

  ![](./media/image11.png)

3. Select **+New**.

  ![](./media/image12.png)

4. Select **Skip** on **Email template** pop-up.

  ![](./media/image13.png)

5. Select the **Content Ideas** icon (3rd icon) in the email editor toolbox.

   ![](./media/image14.png)

6.  If your email is not empty (contains at least 10 words), the copilot, based on your email content, will automatically fill in recommended **key points** to generate new ideas. You can then refine them according to your needs.

7. If your email is empty (or contains fewer than 10 words), choose the **Topic of your email** from the list of suggested topics. For example, select **Event Invitation**.

   ![](./media/image15.png)

8. If you select one of the suggested topics, Copilot automatically fills in sample key points for you, which you can modify according to your needs.

   ![](./media/image16.png)

9. Select the **Tone of voice - Engaged**.

   ![](./media/image17.png)

10. Select **Get ideas**.

  ![](./media/image18.png)

11. Copilot generates a set of text suggestions. It might take a short while to generate content (up to 15 seconds, depending on the usage).

   ![](./media/image19.png)

12. In the generated content, select **+Add to my draft** and then select **+Add element here** in the Email Body.

   ![](./media/image20.png)

13. Browse the generated ideas using the scrollbar in the **Content ideas** pane.

14. You can select **Get more ideas** to generate more ideas for the same key points.

  ![](./media/image21.png)

## Task 3: Use the theme Copilot assistant

1. Select **Theme** from the Email editor toolbox.

  ![](./media/image22.png)

2. Select **+ icon**.

  ![](./media/image23.png)

3. Select the box (empty white box) and select the **blue** color.

   ![](./media/image24.png)

4. If you're happy with the result, you can **save** your email theme. If you want to make further adjustments, you can edit the style of your email elements using the theme pane.

   ![](./media/image25.png)

5. Double-click on the **Company address** in the Email body area. Click on **Company address** under **Compliance**.

   ![](./media/image26.png)

6. Select the **Facebook URL** under **Brand profile**.

  ![](./media/image27.png)

7. Select **Save**.

   ![](./media/image28.png)

8. Expand the first section of the email.

  ![](./media/image29.png)

9. Enter the following information and then select **Save**.
    - **Sender**: Search and select the Default Brand sender
    - **Subject**: ***Test mail***

 ![](./media/image30.png)

10. Select **Preview and test**.

  ![](./media/image31.png)

11. Select the **More options** (three dots) and select **Test send.**

   ![](./media/image32.png)

12. Enter your email id and select **Test send.**

  ![](./media/image33.png)

13. Select **Ready to send**.

  ![](./media/image34.png)

## Summary
In this lab, you learned how to enable Copilot in Customer Insights – Journeys, generate AI-based content suggestions for email creation, and use the theme assistant to style and brand your email layout. You also configured sender details, added compliance and brand profile components, and performed preview/testing steps to validate the final email.
