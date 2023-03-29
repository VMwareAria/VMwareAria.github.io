# Pre Requisites

Before you can start on this, make sure you have done all Pre Requisutes. We need to do some 

- Add Tags in vSphere
- Import Custom groups
- Import a View
- Import two dashboards

You can find all [pre requisites tasks HERE](/files/import/README.md)

# Creating your Monday Morning Dashboard  

We are going to create a dashboard showing all necessary information for troubleshooting purposes, the goal is to make it look like this:

![image-20230328221810409](images/image-20230328221810409.png)

![image-20230328221849201](images/image-20230328221849201.png)

## Aria Operations Dashboard Creation

1. Go to **Dashboard tab** and select from **Dashboards** menu (on the left) **Create Dashboard.** <img src="images/image-20230328201159056.png" alt="image-20230328201159056" style="zoom:67%;" />

2. Select **Object List** 

3. Provide **name** "Select your Application/Environment" 

4. Change Self Provider to **On**

5. Change Auto Select First Row to **On**

   <img src="images/image-20230328201628554.png" alt="image-20230328201628554" style="zoom:80%;" />

6. Expand the Output Filter 

7. Select all these **Object Types**: 
   Environment
   Function
   OPS Exp
   vSphere World

8. Click **save**.

<img src="images/image-20230328204106898.png" alt="image-20230328204106898" style="zoom:50%;" />



##### Note: A detailed description on how to do a very normal selection list can be [found here](/files/selectionlist/README.md)



5. Next, Drag and drop a Heatmap widget onto the canvas.

   ![image-20230328204424379](images/image-20230328204424379.png)

   6. Rename the heatmap to "VMs up or down?"

      <img src="images/image-20230328204535028.png" alt="image-20230328204535028" style="zoom:50%;" />

   7. Select values as per screen shot
      ![image-20230328205001787](images/image-20230328205001787.png)

6. Drop **Alert Volume** and **Top Alerts** widgets onto the canvas

7. Add a new **View widget** - If you can’t see VIEW widgets, please ask!!!

8. Name the View widget: "**Utilization list**", 

9. In the Output Data section below, scroll and select `**Performance|Utilization|VM list**.` 

   ![image-20230328213541259](images/image-20230328213541259.png)

   

   ##### Note: We will now Add multiple View widgets to show different type of performance views and edit the values. 

- Add a new View widget with the name: **CPU performance view** 
- In the Output Data section below, scroll and select : `Performance|Utilization|VM CPU`

![image-20230328210113992](images/image-20230328210113992.png)

- Add a new View widget with the name: **Guest memory Performance**

- In the Output Data section below, scroll and select : `Performance|Guest OS Memory`

<img src="images/image-20230328210608772.png" alt="image-20230328210608772" style="zoom:67%;" />

- Add a new View widget with the name: **disk throughput performance **
- In the Output Data section below, scroll and select : `Performance|Utilization|VM Disk Troughput (total)`

<img src="images/image-20230328210753467.png" alt="image-20230328210753467" style="zoom:67%;" />

11. 
11. Add a new View widget with the name: **OS uptime** 
11. In the Output Data section below, scroll and select:  `Availablity|Guest OS Uptime`

![image-20230328211112779](images/image-20230328211112779.png)

12. Add a new View widget with the name: **Potential cost savings** 

12. In the Output Data section below, scroll and select: `Cost|VM Potential Savings`

    ![image-20230328214707961](images/image-20230328214707961.png)

    13. Add **Heatmap** widget and name it: **workload and contention**

    13. For our output data:

        - Configuration: load/contention

        - Name: **load/contention**

        - Group by: **Virtual Machine** 

        - Mode: **General**

        - Object Type: **Virtual Machine** 

        - Size by: `CPU|Workload (%)`

        - Color by: `CPU|Contention(%)`
          ![image-20230328215223151](images/image-20230328215223151.png)
          
          14. Add an O**bject Relationship (Advanced)** widget with the name: **Object**
              ![image-20230328215423302](images/image-20230328215423302.png)
              
          14. Add Add a **Topology Graph** widget Named: **Topo Graph** 
    
              ![image-20230328215720675](images/image-20230328215720675.png)

Conclusion: This is how we create a dashboard from scratch. Don’t Worry if it’s not finished in time, like a professional tv-cook, we got you covered. Have a look at the dashboard called “”



# Interactions



1. Click the **Show Interactions** tab

   ![image-20230328211241747](images/image-20230328211241747.png)

   2. Create interaction between **Select Your Application** Select widget and all the rest of the widgets on your canvas, This can be done by dragging from your selection list, the arrow, onto the circle of the next widget.

      ![image-20230328221153371](images/image-20230328221153371.png)



3. Instead of Drag’n’Drop between the Select Utilization List and other objects, you can **click** the arrow on you selection list and create interactions with the listed widgets that appears. 

   <img src="images/image-20230328221310534.png" alt="image-20230328221310534" style="zoom:50%;" />

   4. When all the interactions are done click **SAVE** to Save changes

      ![image-20230328221555472](images/image-20230328221555472.png)

      

Conclusion: Dashboards present a visual overview of the performance and state of objects in your virtual infrastructure. You create dashboards by adding widgets to a dashboard and configuring them. We use dashboards to determine the nature and timeframe of existing and potential issues with your environment. 

# The missing Custom <u>Disk</u> VIEW

We are using a custom VIEW on our dashboard. 

As you can see from the interactions above, the last widget on the third row is called **Disks**. 

To learn how to create this view, [go here](/files/view/README.md)



