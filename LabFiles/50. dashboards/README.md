# Create Dashboard

Dashboards present a visual overview of the performance and state of objects in your virtual infrastructure. You use dashboards to determine the nature and timeframe of existing and potential issues with your environment. You create dashboards by adding widgets to a dashboard and configuring them.

As a part of this lab we are going to build custom dashboard which will allow us to see performance data for selected application, this will simplify troubleshooting. 

The goal is to create a dashboard that will look like this: 





![image-20230917205935473](./assets/image-20230917205935473-4977178.png)

In **Visualize** section select **Dashboards**.

![image-20230917210158421](./assets/image-20230917210158421-4977322.png)

Click on **+ Create** to start building dashboard. 

![image-20230917210420603](./assets/image-20230917210420603-4977462.png)

New blank dashboard canvas opens. Provide dashboard name by replacing **New Dashboard** name with your **FirstNameLastName MonMorning** . 

**Note:** <u>This is very important step to name your dashboard properly. The lab is hosted on one VMware Aria Operations instance and having multiple dashboards with the same name can cause issues!</u> 

### Create Application Selection Filter

![image-20230917211633928](./assets/image-20230917211633928-4978195.png)

1. Confirm that you renamed the dashboard to your "FirstNameLastName Mon Morning" as per exaple. 
2. Select **Object List** widget and drop it down to canvas. 
3. Click on **pencil icon** to edit. 

![image-20230917212036232](./assets/image-20230917212036232-4978438.png)

1. Provide **List Object name** "Select your Application/Environment".

2.  Change **Self Provider and Auto Select First Row** to **On**.

3. Clik on **> Output Filter**. 

   ![image-20230917213918111](./assets/image-20230917213918111-4979559-4979561.png)

1. In **>Output Filter** scroll down the list and make multiple selections:

   ![image-20230917213331915](./assets/image-20230917213331915-4979213-4979215.png)

   ![image-20230917213442274](./assets/image-20230917213442274-4979284.png)

   1. Collaps **Object Types**  and scroll down to find **OPS Exp** object. Click on it to mark it down.

      ![image-20230917213726891](./assets/image-20230917213726891-4979448.png)

   2. Scroll down in the same group and select **vSphere World**. 

   3. Click **SAVE**.

   ### Create VMs Up or Down heatmap 

![image-20230917215842783](./assets/image-20230917215842783-4980726.png)

Dropdown **Heatmap** widget to canvas and click on **pencil** icon to edit.

![image-20230917220336324](./assets/image-20230917220336324-4981017.png)

1. Rename to **"VMs up or down?"**. 
2. Click on **>Output Data**.

![image-20230917220751121](./assets/image-20230917220751121-4981273.png)

In the **Output Data** widow:

1. Type a configuration **Name**: **Virtual** and select **Group by** Virtual Machine. 
2. Uncheck **Focus on Groups**.
3. Select **Object Type** Virtual Machine. 
4. Select **Color by** in search field type **Powered ON** - click on the metric. 

![image-20230917221612090](./assets/image-20230917221612090-4981773.png)

1. Check **Solid Coloring**. 
2. Choose only 2 values on the graph. Select **RED** color for **0** value and **GREEN** for **100** vaule.
3. Click **SAVE**.

### Select multiple default widgets

VMware Aria Operations offers default widgets that represent set of data, those widgets usually do not require changes. 

![image-20230917223005433](./assets/image-20230917223005433-4982609.png)

Drop **Alert Volume** widget and make it smaller than previous widget. 

![image-20230917223236591](./assets/image-20230917223236591-4982757.png)

Drop **Top Alerts** widget and make it smaller. 

### View widget

The key component of a Report or a Dashboard is a View. A View helps you interpret data (such as metrics, properties, policies and symptoms) from a number of perspectives. Those perspectives can be transformed to highlight how the data has historically changed (trend) or how the data may look in the future (forecast) built on the historical trend.In this module we will walk through the creation of custom views in VMware Aria Operations. Successfully creating custom views will ensure we can use VMware Aria Operations to track what is important/critical to the monitoring of our VMware Cloud Infrastructure.

![image-20230917223901798](./assets/image-20230917223901798-4983143.png)

1. Switch to **Views**.
2. Drop few **List** widgets.
3. Click **Pencil** icon to edit. 

![image-20230917225138489](./assets/image-20230917225138489-4983900.png)

1. Change the name to "Utilisation list".
2. Type in filter field "utilization".
3. Find and select **Performance|Utilization|VM** view. 
4. Click on **New list view** on the left panel to edit next widget. 





