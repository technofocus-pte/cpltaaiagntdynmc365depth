---
lab:

title: Use Sales Agent in Outlook

description: Learn how to use Microsoft 365 Copilot in Outlook with Dynamics 365 Sales to generate email summaries, create AI-assisted responses, save insights to CRM records, and access opportunity context directly from Outlook.

duration: 30 mins

leve: 200

islab: True

primarytopics: Sales Agent
---

# Compose emails, view email summary and opportunity summary in Outlook using Sales Agent

## Scenario

You are a sales representative at Contoso who manages customer communications through Microsoft Outlook and Dynamics 365 Sales. Every day, you receive numerous customer emails that require quick analysis, follow-up actions, and personalized responses. To improve productivity and maintain accurate CRM records, you use the Dynamics 365 Sales app in Outlook powered by Microsoft 365 Copilot. In this lab, you will explore how Copilot helps summarize customer emails, save key insights to Dynamics 365, generate AI-assisted email responses, and provide opportunity-related information directly within Outlook to support customer engagement and sales activities.

## Objective

In this lab, you will learn how to use the Dynamics 365 Sales app in Microsoft Outlook with Microsoft 365 Copilot to streamline email management and sales communications. You will generate email summaries, save AI-generated insights to Dynamics 365 records, draft professional email responses using predefined and custom prompts, adjust email drafts using Copilot, and view opportunity summaries related to customers directly from Outlook.

## Overview

Organizations often rely on sales teams to process large volumes of customer communications while maintaining accurate CRM records. Microsoft 365 Copilot and the Dynamics 365 Sales app help sellers work more efficiently by providing AI-generated email summaries, intelligent email drafting capabilities, and contextual sales insights within Outlook.

In this lab, you will:

  - Configure a Power Apps trial environment and verify access to a Dataverse-enabled environment.
    
  - Install and access the Dynamics 365 Sales app in Outlook.
    
  - View Copilot-generated summaries of customer emails and save the summaries to Dynamics 365 records.
    
  - Use predefined response categories and custom prompts to draft email replies with Copilot assistance.
    
  - Refine email drafts by adjusting tone, length, and meeting suggestions.
    
  - View opportunity summaries and sales insights associated with customer records directly in Outlook.
  
  By completing this lab, you will understand how Copilot enhances seller productivity, improves communication quality, and ensures important customer interactions are captured in Dynamics 365 Sales.

## Lab Prerequisites

Before starting this lab, ensure that you have:

- A Microsoft 365 tenant with administrative credentials.

- Access to Microsoft Outlook (Outlook on the web).

- A Power Apps Developer Plan or trial license assigned to your account.

- A Dataverse-enabled environment such as the Sales Trial environment.

- Internet connectivity and a supported web browser (Microsoft Edge, Google Chrome, or equivalent).

- Permissions to install and access Outlook add-ins/apps.

- Dynamics 365 Sales app available in Outlook.

- Sample customer emails available in Outlook for testing email summaries and AI-generated responses.

- Microsoft 365 Copilot and Dynamics 365 Sales capabilities enabled in the lab environment.
  
## Exercise 1: Install and open the Sales app in Outlook

1. In a new tab, open **Outlook** using the link **+++www.outlook.com+++**. Select **Sign in**.

  ![](./media/image1.png)

2. Sign in with your **Office 365 admin tenant** credentials.

  ![](./media/image2.png "Screenshot")

3. Open any of the emails. While in an email, select **more actions(…)** > **Apps**.

  ![](./media/image3.png)

4. If you can see **Sales** under **Apps**, you can directly execute step 13. If not, follow the upcoming steps.

  ![](./media/image4.png)

5. If you don’t see **Sales** under **Apps**, select **More apps**, and then click **Add apps**.

  ![](./media/image5.png)

6.  On the **Apps** page, search for ***Sales*** and then select the **Sales** app.

  ![](./media/image6.png)

7.  Select **Add** on Sales card. Once again, select the **Sales** app and click **Open**.

  ![](./media/image7.png)

8.  If appears, on the **Start using Sales app**, select **Got it**.

9.  Navigate to the **Mails**.

  ![](./media/image8.png)

10. Open any of the emails. While in an email, select the **Apps** icon.

  ![](./media/image9.png)

11. Now you will be able to see the **Sales** app. Select the **Sales** app.

  ![](./media/image10.png)

12. If asked, sign in with your **Office 365 admin tenant** credentials in the pop-up window. If a pop-up appears saying Catch up and draft fast with Copilot, select **Got it**.

  ![](./media/image11.png)

13. To sign in to the Dynamics 365 environment, select your environment from the drop-down menu. For this lab, select the **Sales Trial** environment.

  ![](./media/image12.png)

14. After selecting the Sales trial environment, select **OK**.

  ![](./media/image13.png)

15. You can now use the **Sales** pane.

  ![](./media/image14.png)

## Exercise 2: View and save email summary

### Task 1: View email summary

1. In **Outlook**, open a customer email (any), if not open already.

  ![](./media/image15.png "Screenshot")

2. In the email, open the **Apps > Sales** pane.

  ![](./media/image16.png)

3. The email summary is displayed in the **Key email info** card.

  ![](./media/image17.png)

**Note**: If the email content is less than 1000 characters, the email summary will not be generated, and the Summary of this email card will not be displayed.

### Task 2: Save email summary to CRM

1. In the **Key email info** card, click the ellipses (…) and then select **Save summary to Dynamics 365**.

  ![](./media/image18.png)

2. Under **Select a record**, enter Cafe in the search box, select one of the suggested records or use the search box to find another record.

If there are multiple opportunities related to contact, the Sales app displays a list of suggested opportunities, ranked by AI, to save the summary. In this case, the first opportunity is selected by default.

  ![](./media/image19.png)

**Note**:

  - If the email is already connected to an opportunity, it's selected by default.
  
  - If no opportunity is connected, the top-ranked opportunity, which is determined by the open opportunities available for the account or contact, and the content of the email, will be selected by default.
  
  - When you search for a record, the search results display the record name and the key fields selected by your administrator.
  
  - Your search results will be added to the suggested records list, so you can safely search and try again.
  
  - Currently, you can save the summary to one record using Sales app.
  
  - You can connect to all record types that are enabled for activities and added to Sales app by your administrator.

3. Select **Save**.

  ![](./media/image20.png)

The email summary is saved to CRM as a note to the selected record. All Sales app notes share the same subject: "[AI-generated] Email summary from Sales app" and include the subject of the email itself,
as well as the timestamp when the note was saved.

## Exercise 3: Create an email reply using the Sales app in Microsoft Outlook

### Task 1: Create an email reply using pre-defined categories

1. In **Outlook**, open a customer email and select **Reply**.

  ![](./media/image21.png)

2. Select **Apps** from the top bar and then select **Sales**.

  ![](./media/image22.png)

3. If asked, select **Sales** as shown in the image.

  ![](./media/image23.png)

4. Review the information displayed in the **Key email info** card.

  ![](./media/image24.png)

5. Select **Draft an email**.

  ![](./media/image25.png)

6. **Review** the suggested content. Select any of the suggested content. For example, select **Address a concern**.

To generate a different suggestion, select **More options**, and then select **Try again**. Refine the suggested content, if required. You can also restore the suggested content to the previous version.

  ![](./media/image26.png)

7. Copilot gathers the required information and gives a response.

![](./media/image27.png)

8. Select **Add to email**.

  ![](./media/image28.png)

**Note**: Existing content in the email body is not replaced. The suggested content is prepended to any existing content in the email body.

9. **Edit** the email content as required, and then your email is ready to send. For now, select **Discard** to discard the mail

  ![](./media/image29.png)

### Task 2: Create an email message using a custom prompt

If the pre-defined response categories don't suit your requirements, you can enter a custom prompt to generate suggested content. You can get suggested email content when you reply to a customer email, read an email, or compose a new email.

1. In **Outlook**, open a customer email and select **Reply**.

  ![](./media/image30.png)

2. Select **Apps** from the top bar and then select **Sales**.

  ![](./media/image31.png)

3. Select **Sales**.

![](./media/image32.png)

4. Select **Draft an email**.

  ![](./media/image33.png)

**Note**: Pre-defined response categories are not available while composing a new email. You can only enter a custom prompt or create an email to summarize your sales meeting.

5. In the textbox, enter a phrase to describe the kind of reply you want to send, for example **Send the acceptance** and then select **Create draft**.

  ![](./media/image34.png)

6. **Review** the suggested content.

To generate a different suggestion, select More options, and then select Try again. Refine the suggested content, if required. You can also restore the suggested content to the previous version.

  ![](./media/image35.png)

7. Select **Add to email** to add the content to the new email body.

  **Note**: Existing content in the email body is not replaced. The suggested content is prepended to any existing content in the email body.

  ![](./media/image36.png)

8. **Edit** the email content as required, and your email is ready to send. For now, select **Discard**.

  ![](./media/image37.png)

### Task 3: Adjust the email draft

1. Generate the suggested reply using an appropriate response category.

2. Select **Adjust draft**.

  ![](./media/image38.png)

3. On the **Draft with Copilot** page, select the **Length**, **Adjust tone** and **Suggest a meeting time** tabs as per your requirements and then select **Update**.

  ![](./media/image39.png)

4. **Review** the suggested content. If you want to use it, select **Add to email** and it is ready to send.

To generate a different suggestion, select More options, and then select **Try again**. Refine the suggested content, if required. You can also restore the suggested content to the previous version.

  ![](./media/image40.png)

## Exercise 4: View opportunity summary

1. In **Outlook**, open an email or the scheduled meeting.

2. Open the **Sales** pane. Click **Save email to Dynamics 365**.

  ![](./media/image41.png)

3. On the **First, turn on server-side sync** dialog, select **Turn on**.

  ![](./media/image42.png)

4. On **Connect to a record** page, search for the **andrew** and select the contact using the search box.

  ![](./media/image43.png)

5. Select the contact and click **Save**.

  ![](./media/image44.png)

6. Once the email is saved to the record of the selected contact, a message is displayed on the **Sales** pane.

  ![](./media/image45.png)

7. Select the contact. You will be navigated to the **Contact details** page.

  ![](./media/image46.png)

8. On the **Contact details** page, go to the **Opportunities** area and select one of the opportunities.

  ![](./media/image47.png)

9. The **Opportunity summary** and **Opportunity details** are displayed in the **Opportunity summary card**.

  ![](./media/image48.png)

## Summary

In this lab, you learned how to install and open the Sales app in Outlook, generate AI-based email summaries, and save them to relevant Dynamics 365 records. You also used Copilot to draft replies using predefined categories and custom prompts, refine responses with tone and length adjustments, and view opportunity summaries linked to contacts. These capabilities demonstrate how Copilot integrates Outlook and Dynamics 365 to streamline sales communication and improve data-driven decision-making.
