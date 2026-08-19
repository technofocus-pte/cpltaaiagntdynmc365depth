---
lab:

title: Set up and use the Scheduling Operations Agent for Dynamics 365 Field Service

description: Configure and use the **Scheduling Operations Agent** to optimize technician schedules, prioritize work orders, and improve resource assignment.

duration: 30 mins

level: 300

islab: True

primarytopics: Dynamics 365 Field Service
---

# Set up and use the Scheduling Operations Agent for Dynamics 365 Field Service

## Scenario

Contoso provides field service and maintenance support to customers across multiple locations. The service operations team is responsible for efficiently assigning technicians to customer requests while
ensuring that high-priority issues are addressed promptly. 
To improve scheduling efficiency and reduce manual effort, Contoso has decided to implement the Scheduling Operations Agent in Dynamics 365 Field Service. As a Field Service Administrator, your task is to
configure the Scheduling Operations Agent, prepare scheduling data, and use AI-driven scheduling recommendations to optimize technician assignments and improve customer service response times.

## Overview

Copilot in **Dynamics 365 Field Service** helps service organizations improve scheduling efficiency and respond to customer issues more quickly. The **Scheduling Operations Agent** uses AI to optimize technician
schedule, prioritize work orders, and recommend the best resource assignments based on configured business rules.

## Lab Prerequisites

Before starting this lab, ensure that:

- You have access to a Dynamics 365 Field Service environment.

- You have administrator access to the Power Platform admin center.

- The Field Service application is installed and configured.

- Sample resources and work order data are available in the environment.

- You are signed up using the Microsoft 365 provided credentials.

## **Exercise 1: Set up the Scheduling Operations Agent (preview)**

Enable the Scheduling Operations Agent (Preview) in Dynamics 365 Field Service so that AI-powered scheduling capabilities can be used within the environment.

### **Task 1: Turn on the Scheduling Operations Agent**

Enable the **Scheduling Operations Agent** in **Dynamics 365 Field Service** to streamline service scheduling and optimize resource allocation.

1.  Go to **Power Platform admin center** by navigating to **+++https://admin.powerplatform.microsoft.com+++** and if required, sign in using your given **Office 365 admin tenant** credentials.

2.  From the left navigation pane, select **Manage** > **Environment** and then click on **FieldService Trial**.

    ![](./media/image1.png)

3.  Click on **Environment URL**.

    ![](./media/image2.png)

4.  You will be on the **Field Service** portal. Close the pop-up screen.

    ![](./media/image3.png)

5.  Select **Resources** in the change area.

> ![](./media/image4.png)

6.  From the left pane, select **Scheduling Parameters** > **Resource Scheduling**.

> ![](./media/image5.png)

7.  Go to the **Agents** tab and turn on **Scheduling Operations Agent (Preview)**. Select **Save & Close**.

    ![](./media/image6.png)

### **Task 2: Set properties for bookable resources**

Configure resource settings required by the Scheduling Operations Agent, including scheduling locations, resource visibility, and resource type.

1.  Make sure you are in the **Resources** changing area and then from the left navigation pane, select **Resources**.

    ![](./media/image7.png)

2.  Click on the **Alex** **Baker** resource to open it.

    ![](./media/image8.png)

3.  Select the **Scheduling** tab.

    ![](./media/image9.png)

4.  Make sure **Start Location** and **End Location** are selected as Organizational Unit Address. Note that, **Start Location** and **End Location** must be a value **other** than **Location Agnostic**.

    ![](./media/image10.png)

5.  Make sure **Display on schedule board** is set to **Yes**.

    ![](./media/image11.png)

6.  Select the **General** tab.

    ![](./media/image12.png)

7.  Make sure that the **Resource** **Type** is **User**. Select **Save& Close**.

    ![](./media/image13.png)

### **Task 3: Select an optimization method for booking statuses**

Configure optimization methods for booking statuses so that the **Scheduling Operations Agent** can correctly interpret scheduling constraints and booking behaviors.

1.  In the **Resources** change area, select **Booking Statuses** from the **Booking Settings** section in the left navigation pane.

    ![](./media/image14.png)

2.  Select the **Edit columns** icon from the top-right corner of the screen.

    ![](./media/image15.png)

3.  Select **+Add columns**.

    ![](./media/image16.png)

4.  Enter **Optimization** in the search box and select **Optimization Method**.

    ![](./media/image17.png)

5.  Select **Close**.

    ![](./media/image18.png)

6.  Drag the **Optimization Method** column to the 3^(rd) place.

    ![](./media/image19.png)

7.  Select **Apply**.

    ![](./media/image20.png)

8.  You can see the column added and some fields are empty.

    ![](./media/image21.png)

9.  For each booking status, we need to set the **Optimization Method** property to one of the given values: **Ignore**, **Do not Move** and **Optimize**.    

10. Open the booking statuses one by one, those that do not have any **Optimization Method** property assigned and set the **Optimization Method** property to Ignore. For example, select **Arrived**.

    ![](./media/image22.png)

11. In the **Status** field, select **Ignore** from the drop-down menu.

    ![](./media/image23.png)

12. Select **Save & Close**.

    ![](./media/image24.png)

13. Similarly, do it for all the remaining statuses that do not have any **Optimization Method** property assigned.

    ![](./media/image25.png)

### **Task 4: Schedule Board Productivity Features (Set priority values)**

Define priority values for work order priorities to help the Scheduling Operations Agent determine the relative importance of customer requests.

1.  On the Field Service app, go to the **Settings** area.

    ![](./media/image26.png)

2.  Select **Priorities**.

    ![](./media/image27.png)

3.  Select the **Edit columns** icon from the top-right corner of the screen.

    ![](./media/image28.png)

4.  Select **+Add columns**.

    ![](./media/image29.png)

5.  Enter Priority in the search box and select **Priority Value**.

    ![](./media/image30.png)

6.  Select **Close**.

    ![](./media/image31.png)

7.  Drag the **Priority Value** column to the 3^(rd) place.

    ![](./media/image32.png)

8.  Select **Apply**.

    ![](./media/image33.png)

9.  You can see that the **Priority Value** column is empty. Open the Properties one by one to set Priority **Value**. Click **Emergency**.

    ![](./media/image34.png)
    
10. Set the value 100.

    ![](./media/image35.png)

11. Set the **Priority Value** as follows.

    **High: 80, Low: 10, Medium: 70, Normal: 60 and Urgent: 90**.

    ![](./media/image36.png)

## **Exercise 2: Use the Scheduling Operations Agent (preview)**

In this exercise, you will learn how to use the Scheduling Operations Agent in Dynamics 365 Field Service to optimize resource scheduling, prioritize work orders, and generate AI-powered scheduling recommendations. You will configure the required settings, prepare scheduling data and evaluate the agent's scheduling suggestions to improve operational efficiency and customer service.

1.  On the **Field Service** app, go to the **Service** area.

    ![](./media/image37.png)

2.  Close the pop-up screen.

    ![](./media/image38.png)

3.  In the **Scheduling** section, select **Work Orders**. Select **New**.

    ![](./media/image39.png)

4.  At a minimum, enter information in the following required fields and then select **Save & Close**.

   - **Status**: +++Unscheduled+++
   - **Priority**: +++High+++
   - **Service Account**: Enter +++**Contoso**+++ and select **Contoso Coffee** from the suggestion list.
   - **Work Order Type**: Enter +++**Diagnosis**+++ and select **Diagnosis & Repair** from the suggestion list.

5. In the Contacts section, **Reported by**: Enter +++**Alex**+++ and then select **Alex Baker** from the list
    - **Time from promised**: Select todays date and 8:00 AM time.

    ![](./media/image40.png)
   

    ![](./media/image41.png)

5.  From the left pane, now select **Schedule Board**.

    ![](./media/image42.png)

6.  Close any pop-up screen. It can be of agent related.

   ![](./media/image43.png)

7. On the Scheduling board, select **(…)** 3 dots to see more options and then select **Book**.

   ![](./media/image44.png)

8.  In the **Requirement** field, select any sample from the drop-down list.

    ![](./media/image45.png)

9.  Select **Alex** **Baker** as a **Resource**. Set **today’s** date as the **Start** **date**. Set 8:00 AM **Start time** and then select **Book**.

    ![](./media/image46.png)

10. From the **schedule board**, right-click the **name** and select **Suggest schedule**.

    ![](./media/image47.png)

11. On the **Suggest schedule** pane, enter the following information and then select **Suggest schedule**.

    - **Resource**: Alex Baker
    
    - **Scheduling goal**: Maximize utilization
    
    - **Time range**: Next 2 days
    
    - **Requirements**: Unscheduled Work Order Requirements
    
    - **Scheduling options**: Select **Match required characteristics** only

     ![](./media/image48.png)

     ![](./media/image49.png)

     ![](./media/image50.png)

12. **Agent** is analyzing the schedule.

    ![](./media/image51.png)

13. Review the **suggested schedule**.

    ![](./media/image52.png)

## **Summary**

In this lab, you learned how to enable the Scheduling Operations Agent, configure resource properties, assign optimization methods for booking statuses, and set priority values for scheduling logic. You also created a work order and used the schedule board to generate AI-based schedule suggestions. You learned how the agent streamlines resource scheduling and improves scheduling accuracy in Dynamics 365 Field Service.
