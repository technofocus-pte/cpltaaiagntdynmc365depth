---
lab:

title: Use the Sales app in Microsoft Teams and use the conversation intelligence dashboard (preview)

description: Explore how Sales and Copilot integrate with Microsoft Teams to enhance seller productivity through AI-powered meeting insights. Analyze conversation intelligence KPIs and insights using Dataverse-connected dashboards.

duration: 30 mins

level: 200

islab: True

primarytopics: Sales
---


# Use the Sales app in Microsoft Teams and use the conversation intelligence dashboard (preview)

## Scenario

As a sales manager at Contoso, you need to ensure that your sales team is effectively engaging with customers and capturing valuable insights from conversations. To improve collaboration and sales productivity, you use Microsoft Teams integrated with Microsoft 365 Copilot for Sales. By leveraging the Sales app in Teams, you can access CRM data, schedule and manage customer meetings, capture AI-generated meeting recaps and transcripts, and analyze seller conversations through Conversation Intelligence dashboards. In this lab, you will explore how Teams, Dynamics 365 Sales, and Copilot work together to provide actionable sales insights and improve customer engagement.

## Objective & Overview

In this lab, you will learn how to install and configure the Sales app in Microsoft Teams, enable Copilot for Sales capabilities through Teams app setup policies, schedule and manage Teams meetings with sales insights, generate AI-powered meeting transcripts and recaps, and analyze conversation data using the Conversation Intelligence dashboard in Power BI.
Microsoft 365 Copilot for Sales extends the capabilities of **Dynamics 365 Sales** into Microsoft Teams, allowing sellers to access customer information, collaborate more effectively, and gain insights from customer interactions without leaving their workflow. The integration of Teams, Dynamics 365 Sales and Power BI enables organizations to transform customer conversations into actionable business intelligence.

In this lab, you will:

  - Configure a custom Teams app setup policy and install the Sales app in Microsoft Teams.

  - Pin the Sales app for easy access and enable Copilot for Sales experiences.
    
  - Schedule and manage Microsoft Teams meetings integrated with Sales insights.
    
  - Record meetings and generate AI-powered transcripts, recaps, and sales-related insights.
    
  - Explore the Copilot for Sales Conversation Intelligence Dashboard in Power BI.
    
  - Analyze coaching opportunities, customer sentiment, and conversation recordings.
    
  - Connect the dashboard to a Dataverse environment and visualize organizational sales conversation data.

By the end of this lab, you will understand how Copilot for Sales enhances collaboration, meeting effectiveness, seller coaching, and data-driven decision-making through Microsoft Teams and Power BI.

## Lab Prerequisites

 Before starting this lab, ensure that you have:
 
   - A Microsoft 365 tenant with administrative credentials.
      
   - Access to Microsoft Teams Admin Center and Microsoft Teams.
      
   - Microsoft Teams licensing with meeting recording and transcription capabilities enabled.
      
   - Microsoft 365 Copilot for Sales/Sales app available in your environment.
      
   - Permissions to create and manage Teams app setup policies.
      
   - A Dataverse-enabled Dynamics 365 Sales environment, such as a Sales Trial environment.
      
   - Access to Outlook on the web for scheduling Teams meetings.
      
   - Power BI access with permission to install Power BI apps.
      
   - Access to the Copilot for Sales Conversation Intelligence Dashboard from Microsoft AppSource.
      
   - Appropriate permissions to connect Power BI to Dataverse using OAuth authentication.
      
   - A stable internet connection and a supported web browser such as Microsoft Edge or Google Chrome.

## Exercise 1: Install and pin Microsoft Copilot for Sales in Teams

### Task 1: Create a custom Teams app setup policy

1.  Sign in with your given Office 365 credentials to the **Microsoft Teams admin center** using +++ https://admin.teams.microsoft.com/dashboard +++.

2.  In the left pane, select **Teams apps > Setup policies**.

    ![](./media/image1.png)

3.  On the **Manage policies** tab, select **Add**.

    ![](./media/image2.png)

4.  Enter **Assign Copilot permissions** in the **Name** field.

5.  Turn on **User pinning**.

    ![](./media/image3.png)

6.  Under **Installed apps**, select **Add apps**.

    ![](./media/image4.png)

7.  In the **Add installed apps** panel, search for the **Sales** app. You can also filter apps by app permission policy

    ![](./media/image5.png)

8.  Hover the mouse over **Sales** and click on **Select**.

    ![](./media/image6.png)

9.  Select **Add** again to install the listed apps.

    ![](./media/image7.png)

10. Under **Pinned apps**, select **Add apps**.

    ![](./media/image8.png)

11. In the **Add pinned** apps panel, search for the **Sales** app. Hover the mouse over **Sales**, then click **Select**.

    ![](./media/image9.png)

12. Select **Add** again to pin the listed apps.

    ![](./media/image10.png)

13. You can arrange the apps in the order that you want them to appear in Teams.

    ![](./media/image11.png)

14. Once you moved the app to the first place, select **Save**.

    ![](./media/image12.png)

15. Select **Save** on the **User pinning** pop-up window.

    ![](./media/image13.png)

16. From the **Microsoft Teams admin center** portal, select **App launcher** and then select **Teams**.

    ![](./media/image14.png)

17. You can see the **Sales** app pinned in **Teams**.

18. If you don’t see the app pinned, select **View more apps** from the left side pane, search for **Sales** and select **Add**.

    ![](./media/image15.png)

19. The **Sales** app is now ready.

    ![](./media/image16.png)

### **Task 2: Schedule a Microsoft Teams meeting from Outlook**

1. Go to **App launcher**.

    ![](./media/image17.png)

2. Select **Outlook**.

    ![](./media/image18.png)

3. Select **Calendar** from the left navigation pane. Select **New event \> Event**.

    ![](./media/image19.png)

4. Give the name to the meeting – **Sales app Test Meeting**, select the current date and select time (set it to 10 minutes later from the current time).

    ![](./media/image20.png)

5. In the field of **Invite attendees**, enter **your email id**. Ensure that the **Teams meeting** toggle button is **on**. Now select **Send**.

    ![](./media/image21.png)

6. Now go to the **Teams** app, select **Calendar**. You can see the newly scheduled meeting. Click on the meeting.

    ![](./media/image22.png)

7. Select **Edit**.

    ![](./media/image23.png)

8. Select the **Apps icon** from the menu bar at the top.

    ![](./media/image24.png)

9. Search for **Sales** and select it.

    ![](./media/image25.png)

10. Select **Add**.

    ![](./media/image26.png)

11. On the screen that states **This app may have issues**, select **Show the app anyway**.

    ![](./media/image27.png)

12. Select **Save**.

    ![](./media/image28.png)

13. Select **Join** to join the meeting.

    ![](./media/image29.png)

14. If asked, allow the use of headphones for this time. Select **Join now**.

    ![](./media/image30.png)

15. Select **Continue on this browser**.

    ![](./media/image31.png)

16. You will get a notification from the MOD Admin for joining the meeting from your personal Teams app. Select **Join**.

    ![](./media/image32.png "Screenshot")

17. Mute the audio and select **Join now**.

    ![](./media/image33.png)

18. On the Mod Admin’s Team web app, you will get a notification that **Waiting in the lobby**. Select **Admit**.

    ![](./media/image34.png)

19. Select **More > Record** and **Transcribe > Start recording**.

    ![](./media/image35.png)

20. Keep the language **English** and then select **Confirm**.

    ![](./media/image36.png)

21. You can talk about something as a MOD Admin to generate a transcript. (Example - You can explain what Sales in Microsoft 365 is)

22. Leave the meeting from Mod Admin’s Teams web app and your Teams app.

    ![](./media/image37.png)

23. Select **Got it**.

    ![](./media/image38.png)

24. In the Chat section, you can see the recap.

    ![](./media/image39.png)

25. Select **View recap**.

    ![](./media/image40.png)

26. Scroll down and select the **Sales** tab.

    ![](./media/image41.png)

27. You can see sales related insights.

    ![](./media/image42.png)

28. Select **Transcript**, and you can see the AI-generated transcript.

    ![](./media/image43.png)

## Exercise 2: Analyze your sellers' conversation data with Power BI (preview)

### Task 1: Download the Copilot for Sales dashboard app

1. To download the Copilot for Sales - Conversation intelligence dashboard, go to **+++https://go.microsoft.com/fwlink/p/?linkid=2259835+++**. Select **Get it now**.

   ![](./media/image44.png)

2. Enter the given Office 365 tenant credentials and select **Sign in**.

    ![](./media/image45.png)

3. Select **Get it now**.

    ![](./media/image46.png)

4. Again, enter the given Office 365 tenant credentials and select **Submit**.

    ![](./media/image47.png)

5. You will be navigated to Power BI Apps. Select **Install** on the 'Install this Power BI app' window.

    ![](./media/image48.png)

6. You can see the Copilot for Sales - Dashboard under the Apps list. Click on the **Copilot for Sales - Dashboard** to open it.

    ![](./media/image49.png)

7. The following pages are available in your report:

    - Coaching opportunities

    - Customer insights

    - Call recordings

    ![](./media/image50.png)

8. You can use the **Time period filter** and **Data filters** in your report.

    ![](./media/image51.png)

9. Select the **Coaching opportunities page** from the left pane. It displays conversational KPIs and summary charts for the selected time period.

    ![](./media/image52.png)

10. Select the **Customer insights page** from the left navigation pane. It displays customer sentiment and the top brands that your customers are talking about.

    ![](./media/image53.png)

11. Select the **Conversation recordings** page from the left navigation pane. This page helps you listen to call recordings and understand the context of the conversation.

    ![](./media/image54.png)

### Task 2: Connect the dashboard to your organization's data

When you download Copilot for Sales - Conversation intelligence dashboard from Microsoft AppSource, it includes sample data. To connect the dashboard to your own data in Dataverse, follow these steps:

1. Considering the downloaded Copilot for Sales dashboard is open already, select **Connect your data**.

    ![](./media/image55.png)

2. Enter the following information:

    a. **Environment Path**: URL to your Sales trial Dataverse environment. You must remove the prefix from the environment path URL you enter. To get URL, go to Power Platform admin center. Select **Manage** > **Environments** from the left navigation pane, click on **Sales > trial**, and copy the **Environment URL**.
    
    b. **CRM type**: Type of CRM you're using - **Dynamics**.

    c. Select **Next**.

    ![](./media/image56.png)

3. Select an authentication method - **OAuth2** and privacy level settings - **None** for your data source. Select **Sign in and connect**.

   ![](./media/image57.png)

4. After the dashboard is connected successfully to the organization's data, you can edit the report and publish it.

   ![](./media/image58.png)

## **Summary**

In this lab, you learned how to install and pin the Sales app in Teams, schedule meetings with integrated Sales features, and capture AI-generated recaps, transcripts, and sales insights directly inside Teams. You also downloaded the Copilot for Sales conversation intelligence dashboard, explored its KPIs and insights, and connected it to your Dataverse environment to visualize real conversation data. These capabilities demonstrate how Teams, Sales, and Copilot work together to enhance seller productivity and data-driven decision-making.
