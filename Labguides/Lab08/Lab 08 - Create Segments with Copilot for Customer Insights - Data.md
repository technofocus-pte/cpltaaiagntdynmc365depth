---
lab: 8

title: Create segments with Copilot for Customer Insights – Data

description: Learn how to use Dynamics 365 Customer Insights - Data and Copilot to unify customer data, create enriched customer profiles, and build AI-assisted customer segments for deeper audience insights and engagement.

duration: 30 mins

level: 300

islab: True

primarytopics: Dynamics 365 Customer Insights - Data
---
# **Lab 08 - Create segments with Copilot for Customer Insights – Data**

## **Scenario**

Contoso Grocery wants to gain a deeper understanding of its customers by combining customer profile data with transaction history from multiple sources. As a Customer Data Analyst, you need to prepare and unify customer and transaction data in Dynamics 365 Customer Insights – Data, generate a single customer view, and use Copilot to quickly create intelligent customer segments. These segments will help marketing and business teams identify target audiences for personalized campaigns, loyalty programs, and customer engagement initiatives.

## **Objective**
In this lab, you will learn how to prepare and unify customer data in Customer Insights – Data, configure data types using Power Query, define primary keys and matching rules, and generate unified customer profiles. You will also learn how to use Copilot to create AI-assisted segmentation rules that automatically identify targeted customer groups based on behavioral and transactional data.

## **Overview**

Dynamics 365 Customer Insights – Data enables organizations to unify data from multiple sources and create comprehensive customer profiles. In this lab, you will first import customer and transaction data using Power Query and perform data preparation tasks such as assigning column headers and data types. You will then configure unification settings, including primary keys and matching rules, to generate unified customer profiles.
After creating the unified customer data model, you will use Copilot to create customer segments by describing target audiences in natural language. Copilot will generate segmentation rules that help identify relevant groups of customers, enabling faster audience creation and improved customer engagement strategies.

## **Prerequisites**

Before starting this lab, ensure that you have:

 - A provisioned Dynamics 365 Customer Insights – Data environment.
 
 - Access to the Customer Insights – Data application.
 
 - A Microsoft 365 or Dynamics 365 administrator account with appropriate permissions.
 
 - The lab files available in C:\Labfiles:
   - Grocery_Contacts.csv
   - Grocery_transaction.csv
 
 - An internet connection and supported web browser.
 
 - Basic knowledge of customer data, data transformation concepts, and Dynamics 365 Customer Insights terminology.

## **Exercise 1: Add your Data**

In this exercise, you will import customer and transaction datasets into Customer Insights - Data, use Power Query to transform and standardize source data, configure appropriate data types, and create data sources that are ready for customer profile unification.

1. Access your **Customer Insights - Data** environment using the given link **+++https://home.ci.ai.dynamics.com/+++**.

2. Select Individual consumers (B2C) card.

    ![](./media/image57.png)

  **Note**: Close the pop-up – introducing Copilot in Customer Insights – Data.

   ![](./media/image1.png)

3. From the left navigation, select **Data** > **Data sources**.

   ![](./media/image2.png)

3. Select **Add a data source**.

   ![](./media/image3.png)

4. Select **Microsoft Power Query**.

   ![](./media/image4.png)

5. Enter **+++GroceryContacts+++** in the **Data source name** for the data source and select **Next**.

   ![](./media/image5.png)

6. On the **Choose data source** page, select **Text/CSV**.

   ![](./media/image6.png)
   
   **Note**: **When you select **Upload file**, an error message may appear stating that your account does not have a SharePoint Online or OneDrive for Business license. If this error appears, follow the steps (a to e) mentione below to resolve it.**

 a. Open **File Explorer** and select **OneDrive** from the left navigation pane.

   ![](./media/image58.png)

b. Enter your tenant account email address and select **Sign in** to sign in to **OneDrive**.

   ![](./media/image59.png)

c. Enter the **administrator password** provided in the lab and select **Sign in** to continue.

   ![](./media/image60.png)

d. When prompted to **sign in** to all apps and websites on the device, select **No, this app only** to continue without registering the device with your organization.

   ![](./media/image61.png)

e. Leave the default **OneDrive** folder location unchanged. Do not select **Next** or make any changes on this screen.

   ![](./media/image62.png)

7. On the **Connection settings** page, select **Upload file** and then select **Browse**.

   ![](./media/image7.png)

8. Select **Grocery_Contacts.csv** from **C:\Labfiles** in your lab **VM**. Select **Open**.
 
   ![](./media/image8.png)

9. Select **Sign in** to log in to your account.

   ![](./media/image9.png)

10. Enter your **Office 365 admin tenant** credentials.

   ![](./media/image10.png "Screenshot")

11. Select **Next**.

   ![](./media/image11.png)

12. On the **Preview file data** page, select **Transform data**.

   ![](./media/image12.png)

13. On the **Transform data** page, go to the **Transform** ribbon and then select the **Use first row as headers \> Use first row as headers** option.

   ![](./media/image13.png)

14. Right-click the **birthdate** column, go to **Change type**, and then select **Date**.

   ![](./media/image14.png)

15. Select the following columns by holding down the **Ctrl** key on your keyboard: **annualincome**, **msrc_creditscore**, **msrc_customerrelationshipduration**, and **msrc_distancetoneareststore**.

16. When these columns are highlighted, right-click one of them, go to **Change type**, and then select **Decimal number**.

   ![](./media/image15.png)

17. Under **Properties** on the right side, change the **Name** ***contact*** and then press the **Enter** key on your keyboard.

   ![](./media/image16.png)

18. Select **Next**.

   ![](./media/image17.png)

19. Wait till the **Data source** is added successfully.

   ![](./media/image19.png)

20. On the **Data sources** page, select **Add a data source**.

   ![](./media/image20.png)

21. Select **Microsoft Power Query**.

   ![](./media/image21.png)

22. Enter ***+++GroceryTransactions+++*** in the **Data source Name** for the data source and select **Next**.

   ![](./media/image22.png)

23. On the **Choose data source** page, select **Text/CSV**.

   ![](./media/image23.png)

24. On the **Connection settings** page, select **Upload file** and then select **Browse**.

   ![](./media/image24.png)

25. Select **Grocery_transaction.csv** from **C:\Labfiles** in your lab **VM**. Click **Open**.

   ![](./media/image25.png)

26. Once the file is uploaded, select **Save**.

   ![](./media/image26.png)

27. On the **Preview file data** page, select **Transform data**.

   ![](./media/image27.png)

28. As before, go to **Transform** and select **Use first row as headers > Use first row as headers**.

   ![](./media/image28.png)

29. Scroll to and select the **msrc_transactiontimestamp** column. Right-click the column, select **Change type**, and then select **Date/Time**.

   ![](./media/image29.png)

30. Press and hold the **Ctrl** key on your keyboard to select the **msrc_transactionamount** and **msrc_discountappliedamount** columns. Right-click one of the columns, go to **Change type**, and then select **Decimal number**.

31. Select **Next**.

   ![](./media/image31.png)

32. On the **Refresh settings** page, select **Refresh manually**. Select **Save**.

   ![](./media/image32.png)

33. Wait till the **Data source** is added successfully.

   ![](./media/image33.png)

## **Exercise 2: Unify your data**

In this exercise, you will unify customer and transaction data by selecting source tables, defining primary keys, configuring matching rules, and generating unified customer profiles that provide a consolidated view of customer information across multiple data sources.

1. In **Customer Insights - Data**, expand **Data** in the left navigation pane and then select **Unify**.

   ![](./media/image34.png)

2. Select **Get started** on the **Customer data** area.

   ![](./media/image35.png)

3.  On the **Describe the customer data to be unified** page, select the **Select tables and columns** button.

    **Note**: Select (…) 3 dots in the top bar if you don’t see the given option due to screen resolution.

    ![](./media/image36.png)

    ![](./media/image37.png)

4. Select the **contact** and **Grocery_transaction** tables and then select **Apply**.

    ![](./media/image38.png)

5. Select the **contact** table and then select **contactid** as the primary key.

   ![](./media/image39.png)

6. Select the **Grocery_transaction** table and then select **msrc_transactionid** as the primary key. Select **Next**.

   ![](./media/image40.png)

7. On the **Define deduplication rules** page, click **Next**.

   ![](./media/image41.png)

8. On the **Define matching rules** page, set up the tables in the following order: **contact** and **Grocery_transaction**.

9. Ensure that the **Include all records** checkbox is selected for all tables.

   ![](./media/image42.png)

10. Select **+ Add rule** next to the **Grocery_transaction** table.

   ![](./media/image43.png)

11. Select **contactid** and **msrc_customerid** and then name the rule **+++contacttransactions+++**. Select **Done**.

   ![](./media/image44.png)

12. Select **Next**.

   ![](./media/image45.png)

13. Review and edit how source data is combined into unified customer fields on the **Unified data view** page. Click **Next**.

   ![](./media/image46.png)

14. On the **Review and create customer profiles** page, select **Create customer profiles**.

   ![](./media/image47.png)

15. This process will take several minutes to complete.

16. Review the **Customer data**, **Deduplication rules**, **Matching rules**, and **Unified data view** fields on the **Unify** page.

    ![](./media/image48.png)

## **Exercise 3: Create segments with Copilot for Customer Insights - Data (preview)**

In this exercise, you will use Copilot to create customer segments through natural language prompts, review and apply AI-generated segment rules, and generate a target audience that can be used for customer analysis, personalization, and engagement activities.

1. In **Customer Insights - Data**, go to **Insights** > **Segments**.

    ![](./media/image49.png)

2. Select + **New segment** to create a segment.

    ![](./media/image50.png)

<!-3. Select the **Copilot** icon to open the **Copilot** pane.

    ![](./media/image51.png)

4. Enter a description of your segment or choose one of the suggested prompts. For example, select **Customers who have a loyalty membership**.
 
    **Note**: If Copilot gives a message that **‘Sorry, I’m having trouble generating insights for this segment’**, then close the Copilot pane. Go to **Step 6**, enter the rule as shown in the image of **Step 5**, and select **Run**.

    ![](./media/image52.png "Screenshot")

5. Select **Use** to apply the result to a rule.

    ![](./media/image53.png "Screenshot") -->


 **Note:** The Create segments with Copilot feature in Customer Insights - Data is no longer available as of November 2, 2026. Use the Segment builder to create the Loyalty membership segment by following the steps below. 

3. Select msrc_loyaltymembership from CustomerInsights under Customer.

   ![](./media/image63.png)

4. Select **is not** from the operator dropdown.

   ![](./media/image64.png)

5. Select **empty** from the value dropdown.

   ![](./media/image65.png)

6. On the Edit details page, enter +++Loyalty membership+++ in the **Name** field, then select **Done**.

    ![](./media/image66.png)

7. Select **Run** to execute the segment definition.

    ![](./media/image67.png)

8. The **Loyalty membership** segment is now created.

    ![](./media/image68.png)

   **Note**: If the resulting segment contains multiple **relationship paths**, it uses the shortest path by default. **Edit** the segment to change the relationship path.

## **Summary**

In this lab, you learned how to load and transform customer and transaction datasets, unify customer records using deduplication and matching rules, and create enriched customer profiles in Customer Insights – Data. You also created customer segments using the Segment builder by defining rules and applying filters to identify customers based on specific criteria.
