
lab: 10

title: Create AI customer journeys with Journey Creation Agent – Journeys

description: Learn how to use the Journey Creation Agent in Dynamics 365 Customer Insights – Journeys to create AI-generated customer journeys, build audience segments with natural language, and publish personalized marketing experiences using Copilot.

duration: 30 mins

level: 300

islab: True

primarytopics: Dynamics 365 Customer Insights- Journeys
---

# **Lab 10 - Create an AI-Assisted Customer Journey with the Journey Creation Agent in Customer Insights – Journeys**

## **Scenario**

You are a Marketing Automation Specialist at Contoso responsible for onboarding new customers and increasing engagement through personalized marketing campaigns. To streamline campaign creation, you will use the **Journey Creation Agent** in Dynamics 365 Customer Insights – Journeys. Using natural language prompts, you will create a target audience, generate an AI-assisted customer journey, review the journey design, and publish a multi-step campaign that automatically sends welcome and follow-up communications to new customers.

In this lab, you will use **Copilot** in Customer Insights – Journeys to build a fully automated, AI-assisted customer journey. You will enable the Journey Creation Agent, create and configure a target segment, generate a multi-step journey from a natural language prompt, review and adjust the Copilot-generated steps, and publish a live, running journey.

## **Objective**

In this lab, you will learn how to:

- Enable and configure the Journey Creation Agent in Dynamics 365 Customer Insights – Journeys.
- Create a customer segment using natural language with Query Assist and Copilot.
- Generate an AI-assisted customer journey from a simple business description.
- Review and refine Copilot-generated journey steps and audience settings.
- Configure automated customer engagement workflows using emails and wait conditions.
- Publish and validate a live customer journey for marketing execution.

## **Overview**

Dynamics 365 Customer Insights – Journeys includes the Journey Creation Agent, an AI-powered capability that helps marketers create complete customer journeys using natural language. In this lab, you will first enable the Journey Creation Agent through the Dynamics 365 AI Hub and verify its availability within Customer Insights – Journeys. You will then create a target segment using Query Assist, allowing Copilot to translate business requirements into audience criteria.

Next, you will use the Journey Creation Agent to generate a customer journey based on a plain-language prompt. The agent automatically creates audience targeting, email activities, wait conditions, and journey flow components. Finally, you will review the generated journey, make any necessary adjustments, and publish it as a live marketing journey that automates customer engagement activities.

# **Exercise 1: Verify Customer Insights – Journeys Licensing and enable Copilot**

## **Task 1: Access Power Platform Admin Center and Verify Environment Configuration**

1. Open a new browser tab, go to +++**https://admin.powerplatform.microsoft.com**+++, and sign in with your Office 365 admin tenant credentials if prompted.

2. From the left navigation pane, select **Manage** > **Environment** and then click on **Marketing trial**.

    ![](./media/image1.png)

3. Click on **Environment URL**.

    ![](./media/image2.png)
  
5. Select **Customer Insights – Journeys**.

    ![](./media/image3.png)

5. Select **Customer Insights – Journeys** if asked.

    ![](./media/image34.png)

## **Exercise 2 - Enable and access the Journey Creation Agent**

Turn on the Journey Creation Agent in the Dynamics 365 AI hub and confirm you can access it from Customer Insights – Journeys before you start building a journey.

1. Go to **Power Platform Admin Center** > **Copilot** > **Settings**. Or, go to this URL: +++**https://admin.powerplatform.microsoft.com/copilot/settings**+++.

     ![](./media/image35.png)
 
2. Scroll to the **Dynamics 365 Customer Insights – Journeys** section.
 
     ![](./media/image36.png)
 
3. Select **AI agents**.

    ![](./media/image52.png) 

4. Under **AI agents**, select the required environment or environment group, and then select **Edit setting**.

    ![](./media/image37.png)
  
5. Turn **AI agents** to **On**, and then select **Save** to apply the changes.

    ![](./media/image38.png)

### **Task 1: Open the AI Hub**

1. Navigate to the **Customer Insights – Journeys portal**. The Welcome to real-time journeys home page opens, displaying quick start tiles for creating emails, journeys, and text messages.

     ![](./media/image40.png)

2. In the left-hand navigation, select **Settings**, then choose **AI hub** to open the area where AI agents are managed.

     ![](./media/image41.png)

### **Task 2: Add Journey Creation Agent**

1. On the Dynamics 365 AI hub page, select **Add and manage agents** under Agent manager.
   
2. Confirm the **Prerequisites** section shows **3 of 3** complete **(Microsoft Copilot Studio capacity, move data across regions, and AI prompts)**.

     ![](./media/image7.png)

3. Select **Add an agent**, then choose the **Journey Creation Agent** card (Preview). This agent automatically generates tailored campaigns and builds customer journeys from natural language. Select **Choose**.

     ![](./media/image8.png)

4. Review the agent **Overview**, which explains that the agent interprets your goal, asks clarifying questions, and builds a complete journey with triggers, steps, and waits. Select **Next**.

     ![](./media/image9.png)

5. On the **Prerequisites** tab, confirm **Anthropic** shows a Done status (this allows the agent to use the underlying AI model), then select Next.

     ![](./media/image10.png)

6. On the **Settings** tab, review the message consumption limit option, then select **Enable** agent.

     ![](./media/image11.png)

7. A confirmation dialog appears once the agent is ready. Select **Got it**, to close it.

     ![](./media/image12.png)

8. Back on the **Agent manager** page, verify that **Journey Creation Agent** now appears in the AI agents list with a Status of Enabled.

     ![](./media/image13.png)

<!--
### **Task 3: Open the Customer Insights – Journeys App**

1.  Go to **+++https://powerapps.microsoft.com+++** and select **Apps** in the left navigation to view the apps available in the environment.
    
  ![](./media/image14.png)

2.  In the apps list, locate **Customer Insights – Journeys** and select the **edit (pencil)** icon to open it, or select the app name to launch it directly.

 ![Apps list with Customer Insights - Journeys edit icon highlighted](./media/image15.png "Apps list with Customer Insights - Journeys edit icon highlighted")

3. The app opens and displays the **Journeys area**. Confirm you can see the **All Journeys list** before moving to the next exercise.

     ![All Journeys list in the app](./media/image16.png "All Journeys list in the app")

-->
## **Exercise 3 – Create a target segment**

Build a segment that identifies new customers who should receive the welcome campaign, so the journey you generate in Exercise 3 has an audience to target.

### **Task 1: Create a New Segment**
 Create a new segment by following the steps below, or use the existing Loyalty membership segment created in Lab 08.
    
1. Select **Customer Insights – Journeys** from the change area, under **Audiences**, select **Segments**, and then select **New segment** to open the segment creation pane.

      ![](./media/image17.png))
  
1. In the Name field, enter +++New Customers - Welcome Campaign+++, and then select **Lead** from the **Select a target audience** drop-down list. Select **Create**.

      ![](./media/image19.png)
   
### **Task 2: Define the Segment Condition**

 1.  On the segment canvas, select **Add a new group**.

       ![](./media/image45.png)
    
 2.  From the drop-down list, select **Behavioral group**.

       ![](./media/image46.png)

 3.  In the **Behavioral** pane, expand **Marketing form**, and then select **Submitted**.

       ![](./media/image47.png)

 4.  Verify that **Marketing Form Submitted at least once in the last 28 days** is added to **Group 1**, and then in the **Marketing Form** Submitted pane, select **E-mail Id**.

       ![](./media/image48.png)

 5.  In the **E-mail Id** row, select the drop-down arrow, and then select **Contains**.

       ![](./media/image49.png)

 6. In the **Enter value** field, enter +++Contoso+++, and then select **Ready to use**.

      ![](./media/image50.png)  
    
 7.  Verify that the **New Customers - Welcome Campaign** segment status changes to **Getting ready**.

        **Note: The segment status shows **Ready to use** once processing completes. The panel also confirms the segment refreshes every 24 hours until it is used in a journey and will expire after 120 days if it remains unused.**

      ![](./media/image51.png) 

 9. Verify that the **New Customers - Welcome Campaign segment** status changes **Ready to use**.

      ![](./media/image20.png)

## **Exercise 4 – Generate the journey with Copilot**

   Use the Journey Creation Agent to turn a plain-language description into a complete, multi-step customer journey that targets the segment created in Exercise 2.

### **Task 1: Start the Journey Creation Agent**

1. Select **Real-time Journeys** from the change area, under **Engagement**, select **Journeys**.

     ![](./media/image53.png)

   **Note: If the Send button is disabled (grayed out), select Skip and create from blank and follow Task 2: Create the Journey Manually instead.**
   
3. The **Create new journey** dialog appears with the **Journey Creation Agent (Preview)** tab selected. The **What would you like to plan today?** prompt is displayed.

     ![](./media/image21.png)

4. In the prompt box, enter: **+++Create a journey that will send a welcome email to all new customers that are part of the New Customers – Welcome Campaign segment. After two days, send them an exclusive offer email.+++** Select the **Send** (arrow) icon.

    ![](./media/image22.png)

5. Select **Allow** to use data and proceed with **generating response**.

    ![](./media/image42.png)

6. Select **Allow** to connect with **Microsoft Dataverse**.

    ![](./media/image43.png)

7. Wait while the agent’s reasons through the request. When it finishes, review the summary it provides, confirming the audience (New Customers - Welcome Campaign segment) and the Welcome Email send step.

8. On the canvas, confirm the generated journey structure: **Journey start > Email (Welcome Email) > Wait (2 days) > Email (Exclusive Offer) > Exit.** Adjust any step if needed before continuing.

      ![Generated journey canvas with Welcome Email, Wait, and Exclusive Offer steps](./media/image23.png "Generated journey canvas with Welcome Email, Wait, and Exclusive Offer steps")

9. Select **Review and publish** in the top-right corner of the journey canvas, then confirm the publishing action.

      ![Generated journey canvas with Welcome Email, Wait, and Exclusive Offer steps](./media/image24.png "Generated journey canvas with Welcome Email, Wait, and Exclusive Offer steps")

10. When the confirmation dialog appears, select **Skip or Tell me more** to close it.

      ![Journey published confirmation dialog](./media/image25.png "Journey published confirmation dialog")

11. Verify that the journey status is **Live** and that a **scheduled start date and time** are displayed.

12. Review the final journey canvas and verify that it includes the **Welcome Campaign** trigger, **Welcome Email**, **2-day wait**, and **Exclusive Offer** email.

      ![Published journey showing Live status](./media/image26.png "Published journey showing Live status")

### **Task 2: Create the Journey Manually (alternative workflow)**

1. In the Create new journey dialog, select **Skip and create from blank**.
    
    ![](./media/image54.png)
   
2. On the **Create a new journey** creation screen, enter a journey name, such as +++**Welcome Journey**+++.

    ![](./media/image55.png)     

3. Select **Segment-based** as the journey type. Select the **New Customers – Welcome Campaign** segment from the list or select **+ New** to create a new segment.

   ![](./media/image56.png)  
        
4. Select **A one-time journey with a static audience** under **Select the frequency**. Then specify the journey's **Start date** and **Start time**.

    ![](./media/image57.png) 

5. Select **Create** to create the journey and open the journey canvas.

    ![](./media/image58.png)

6. On the journey canvas, select the **+ icon** below the Journey start node to add the first journey action.

    ![](./media/image59.png)

7. Under **Messages**, select **Email** to add an email action to the journey.

     ![](./media/image60.png)

8. Under **Select email**, choose the existing **Email 1** template from the list.

    ![](./media/image61.png)

9. Review the selected **Email 1** template in the **Preview pane** to verify the email content.

     ![](./media/image63.png)

10.  On the journey canvas, select the **+ icon** below the **Email 1** action. Under **Conditions**, select **Wait time** to add a delay before sending the next email.

     ![](./media/image62.png)

11. Under **People will wait**, select **A set amount of time** to configure the waiting period.

     ![](./media/image64.png)

12. Set the Duration to **1** and select **days** from the dropdown to configure a one-day waiting period.

     ![](./media/image65.png)

13. Verify that the **Wait** action displays **1 days** on the journey canvas.

      ![](./media/image66.png)
              
14. On the journey canvas, select the **+ icon** below the **Wait** action.
    
     ![](./media/image75.png)

16. Under **Messages**, select **Email** to add an email action to the journey.

     ![](./media/image60.png)

17. Under **Select email**, choose the existing **Email 2** template to the journey.

    ![](./media/image67.png)

18. Review the selected **Email 2** template in the **Preview pane** to verify the email content.

     ![](./media/image68.png)

19. Select **Save** to save the journey configuration.

    ![](./media/image69.png)

20. Select **Publish** to publish the journey and make it live.

    ![](./media/image70.png)
    
22. After publishing the journey, the analytics introduction pop-ups appear. Select **Got it**, then select **Next** on each subsequent screen to proceed through the analytics overview.

     ![](./media/image71.png)

     ![](./media/image72.png)

     ![](./media/image73.png)

23. Verify the **green confirmation message** stating that the** Welcome Journey was successfully published**. Confirm that the journey status displays **Live**.

    ![](./media/image74.png)    

## **Summary**

In this lab, you enabled the Journey Creation Agent in the Dynamics 365 AI hub and confirmed access to it through the Customer Insights – Journeys app. You created a target segment (New Customers - Welcome Campaign) and used Query Assist to define its membership conditions with natural language. You then used the Journey Creation Agent to generate a complete, multi-step journey from a text prompt, reviewed the Copilot-generated steps — a welcome email, a two-day wait, and an exclusive offer email — and published the journey so it is now live and running against your segment. You have practiced the end-of-the-end workflow for building AI-assisted customer journeys with Copilot, from agent setup through publishing.
