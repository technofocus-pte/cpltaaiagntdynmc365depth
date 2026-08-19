<img width="1557" height="862" alt="image" src="https://github.com/user-attachments/assets/bb68e245-9c24-4dab-8d59-768f0e433f30" />---
lab:

title: Create AI customer journeys with Journey Creation Agent – Journeys

description: Learn how to use the Journey Creation Agent in Dynamics 365 Customer Insights – Journeys to create AI-generated customer journeys, build audience segments with natural language, and publish personalized marketing experiences using Copilot.

duration: 30 mins

level: 300

islab: True

primarytopics: Dynamics 365 Customer Insights- Journeys
---

# Create an AI-Assisted Customer Journey with the Journey Creation Agent in Customer Insights – Journeys

In this lab, you will use Copilot in Customer Insights – Journeys to build a fully automated, AI-assisted customer journey. You will enable the Journey Creation Agent, create and configure a target segment, generate a multi-step journey from a natural language prompt, review and adjust the Copilot-generated steps, and publish a live, running journey.

## Enable Copilot in Customer Insights – Journeys**
1. Go to **Power Platform admin center** by navigating to +++ https://admin.powerplatform.microsoft.com +++ and if required, sign in using your given **Office 365 admin tenant** credentials.

2. From the left navigation pane, select **Manage** \> **Environment** and then click on **Marketing trial**.

 ![](./media/image1.png)

3. Click on **Environment URL**.

 ![](./media/image2.png)
  
5. Select **Customer Insights – Journeys**.

![](./media/image3.png)

5. Select **Customer Insights – Journeys** if asked.

 ![](./media/image4.png)

## **Exercise 1 - Enable and access the Journey Creation Agent**

**Objective**: Turn on the Journey Creation Agent in the Dynamics 365 AI hub and confirm you can access it from Customer Insights – Journeys before you start building a journey.

### Task 1: Open the AI Hub

1. Navigate to the **Customer Insights – Journeys portal**. The Welcome to real-time journeys home page opens, displaying quick-start tiles for creating emails, journeys, and text messages.

![Real-time journeys home page](./media/image5.png "Real-time journeys home page")

2.  In the left-hand navigation, select **Settings**, then choose AI hub to open the area where AI agents are managed.

![Settings menu with AI hub highlighted](./media/image6.png "Settings menu with AI hub highlighted")

### Task 2: Add Journey Creation Agent

1. On the Dynamics 365 AI hub page, select **Add and manage agents** under Agent manager. 
2. Confirm the Prerequisites section shows 3 of 3 complete (Microsoft Copilot Studio capacity, Move data across regions, and AI prompts) before continuing.

![Agent manager
prerequisites](./media/image7.png "Agent manager prerequisites")

3. Select **Add an agent**, then choose the **Journey Creation Agent** card (Preview). This agent automatically generates tailored campaigns and builds customer journeys from natural language. Select **Choose**.

![Add an AI agent dialog](./media/image8.png "Add an AI agent dialog")

4. Review the agent **Overview**, which explains that the agent interprets your goal, asks clarifying questions, and builds a complete journey with triggers, steps, and waits. Select **Next**.

![Journey Creation Agent overview](./media/image9.png "Journey Creation Agent overview")

5. On the **Prerequisites** tab, confirm **Anthropic** shows a Done status (this allows the agent to use the underlying AI model), then select Next.

![Journey Creation Agent prerequisites
tab](./media/image10.png "Journey Creation Agent prerequisites tab")

6. On the **Settings** tab, review the message consumption limit option, then select **Enable** agent.

![Journey Creation Agent settings
tab](./media/image11.png "Journey Creation Agent settings tab")

7. A confirmation dialog appears once the agent is ready. Select **Got it**, to close it.

![Agent enabled confirmation
dialog](./media/image12.png "Agent enabled confirmation dialog")

8. Back on the **Agent manager** page, verify that **Journey Creation Agent** now appears in the AI agents list with a Status of Enabled.

![AI agents list showing Journey Creation Agent
enabled](./media/image13.png "AI agents list showing Journey Creation Agent enabled")

### Task 3: Open the Customer Insights – Journeys App

1. Go to **+++https://powerapps.microsoft.com +++** and select **Apps** in the left navigation to view the apps available in the environment.

![Power Apps home page with Apps highlighted](./media/image14.png "Power Apps home page with Apps highlighted")

2. In the apps list, locate **Customer Insights – Journeys** and select the **edit (pencil)** icon to open it, or select the app name to launch it directly.

![Apps list with Customer Insights - Journeys edit icon
highlighted](./media/image15.png "Apps list with Customer Insights - Journeys edit icon highlighted")

3. The app opens and displays the **Journeys area**. Confirm you can see the **All Journeys list** before moving to the next exercise.

![All Journeys list in the app](./media/image16.png "All Journeys list in the app")

## **Exercise 2 – Create a target segment**

**Objective**: Build a segment that identifies new customers who should receive the welcome campaign, so the journey you generate in Exercise 3 has an audience to target.

### Task 1: Create a New Segment

1. Go to **Customer Insights – Journeys \> Audiences \> Segments**.

![All Segments view](./media/image17.png "All Segments view")

2. Select **New Segment** to open the segment creation pane.

![New segment dialog](./media/image18.png "New segment dialog")

3. Name the new segment **New Customers - Welcome Campaign** and select **Lead** from the Select a target audience drop-down list.

![Naming the segment and choosing target audience](./media/image19.png "Naming the segment and choosing target audience")

### Task 2: Define the Segment Condition with Query Assist

1. In the Query Assist box, describe the audience in natural language —for example, **leads whose e-mail address contains Contoso and who submitted a marketing form at least once in the last 28 days** — and let Copilot build the matching condition. Select **Create** to save the segment.

2. Open the **Design** tab of the segment (here shown for the **Welcome Campaign segment**) to review the generated condition group. Confirm it reads: **Marketing Form Submitted** **at** **least once in the last 28 days**, with E-mail Id Contains **Contoso**. In the Segment details pane on the right, confirm the Segment type is Dynamic, and the Target audience is set to Leads.

3. Note that the segment status shows **Ready to use** once processing completes. The panel also confirms the segment refreshes every 24 hours until it is used in a journey and will expire after 120 days if it remains unused.

![](./media/image20.png)

## **Exercise 3 – Generate the journey with Copilot**

**Objective**: Use the Journey Creation Agent to turn a plain-language description into a complete, multi-step customer journey that targets the segment created in Exercise 2.

### Task 1: Start the Journey Creation Agent

1. From the Journeys area, select **New journey**. The Create new journey dialog opens on the Journey Creation Agent (Preview) tab, prompting What would you like to plan today?

![Create new journey dialog with Journey Creation Agent tab](./media/image21.png "Create new journey dialog with Journey Creation Agent tab")

2. In the prompt box, enter: **Create a journey that will send a welcome email to all new customers that are part of the New Customers – Welcome Campaign segment. After two days, send them an exclusive offer email.** Select the **Send** (arrow) icon.

![Prompt entered in Journey Creation Agent](./media/image22.png "Prompt entered in Journey Creation Agent")

### Task 2: Review the Generated Journey

1. Wait while the agent’s reasons through the request. When it finishes, review the summary it provides, confirming the audience (New Customers - Welcome Campaign segment) and the Welcome Email send step.

2.  On the canvas, confirm the generated journey structure: **Journey start \> Email (Welcome Email) \> Wait (2 days) \> Email (Exclusive Offer) \> Exit.** Adjust any step if needed before continuing.

![Generated journey canvas with Welcome Email, Wait, and Exclusive Offer steps](./media/image23.png "Generated journey canvas with Welcome Email, Wait, and Exclusive Offer steps")

## **Exercise 4 – Review and publish the journey**

**Objective**: Publish the completed journey so it goes live and starts
running against the target segment.

### Task 1: Publish the Journey

1. Select **Review and publish** in the top-right corner of the journey canvas, then confirm the publishing action.

![Generated journey canvas with Welcome Email, Wait, and Exclusive Offer steps](./media/image24.png "Generated journey canvas with Welcome Email, Wait, and Exclusive Offer steps")

2. When the confirmation dialog appears, select **Skip or Tell me more** to close it.

![Journey published confirmation dialog](./media/image25.png "Journey published confirmation dialog")

### Task 2: Verify the Journey Is Live

1. Verify that the journey status is **Live** and that a **scheduled start date and time** are displayed.

2. Review the final journey canvas and verify that it includes the **Welcome Campaign** trigger, **Welcome Email**, **2-day wait**, and **Exclusive Offer** email.

![Published journey showing Live
status](./media/image26.png "Published journey showing Live status")

## **Summary**
In this lab, you enabled the Journey Creation Agent in the Dynamics 365 AI hub and confirmed access to it through the Customer Insights – Journeys app. You created a target segment (New Customers - Welcome Campaign) and used Query Assist to define its membership conditions with natural language. You then used the Journey Creation Agent to generate a complete, multi-step journey from a text prompt, reviewed the Copilot-generated steps — a welcome email, a two-day wait, and an exclusive offer email — and published the journey so it is now live and running against your segment. You have practiced the end-of-the-end workflow for building AI-assisted customer journeys with Copilot, from agent setup through publishing.
