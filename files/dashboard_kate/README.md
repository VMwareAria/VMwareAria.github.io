Login to VMware HOL https://labs.hol.vmware.com/HOL/catalogs/lab/10126 

**Creating your Monday Morning Dashboard** 

**I. Import "Everything" (Beng to provide entry steps)**

- Go to 



​	Switch to Import view 

Pre-steps:

1. Login to vCenter server https://vcsa-01a.corp.local/ using user: administrator@vsphere.local password: VMware1!

2. Locate Workload 1 Cluster. Repeat for All the VMs steps below

   <img src="image-20230328165757425.png" alt="image-20230328165757425" style="zoom:67%;" />

   3. Locate VM object and **right click**, Select **Tag & Custom Attributes** next select **Assign Tag...** 

      <img src="image-20230328171250303.png" alt="image-20230328171250303" style="zoom:67%;" />

      4. Confirm by clicking OK 

         <img src="image-20230328171941176.png" alt="image-20230328171941176" style="zoom:50%;" />

         

      5. Select Create Category named **"Exp Day"** select **Many tags option.

         <img src="image-20230328180428944.png" alt="image-20230328180428944" style="zoom:67%;" /> 

      6. Create Tag by choosing **OPS Exp**Category.

         <img src="image-20230328180735145.png" alt="image-20230328180735145" style="zoom:70%;" />

         

      7. Assign above tag to All VMs in Worload 1 cluster. 

         

         

Import file Name "Content-2023-03-27 09-31-54 AM.zip" password to file VMware1!VMware1!

Create a Custom Group 

1. Create a group type

   1. Go to Administration 

      ![image-20230328181642530](image-20230328181642530.png)

   2. Next select **Group Types** and click on **ADD**

      <img src="image-20230328181957890.png" alt="image-20230328181957890" style="zoom:67%;" />

   3. Name it OPS Exp

      ![image-20230328182104832](image-20230328182104832.png)

   4. Go to Envronment tab, select Custom Groups and ADD new one

   5. Provide New group name "Ops Exp Day" and assign the **Group Type OPS Exp**, assign Policy: HOL Policy and check **Keep group membership up to date**. Define membership criteria by choosing **Virtual Machine** object, then select Tag name the **Tag category** as "appowner" select **contains** "Kate".

   ![image-20230328203124468](image-20230328203124468.png)

   

   

**II. Create Dashboard** 

We are going to create a dashboard showing all necessary information for troubleshooting purposes, the goal is to make it look like this:

![image-20230328221810409](image-20230328221810409.png)

![image-20230328221849201](image-20230328221849201.png)

1. Go to **Dashboard tab** and select from **Dashboards** menu (on the left) **Create Dashboard.** <img src="image-20230328201159056.png" alt="image-20230328201159056" style="zoom:67%;" />

2. Select List Object 

3. Provide **List Object name** "Select your Application/Environment" and change **Self Provider and Auto Select First Row** to **On**

   <img src="image-20230328201628554.png" alt="image-20230328201628554" style="zoom:80%;" />

4. In **Optput Filter** Select **Object Types: Environment, Function, OPS Exp and vSphere World** save.

<img src="image-20230328204106898.png" alt="image-20230328204106898" style="zoom:50%;" />

5. Drag and drop Heatmap widget.

   ![image-20230328204424379](image-20230328204424379.png)

   6. Rename to "VMs up or down?"

      <img src="image-20230328204535028.png" alt="image-20230328204535028" style="zoom:50%;" />

   7. Select values as per screen shot. 

      ![image-20230328205001787](image-20230328205001787.png)

8. Drop on the canvas Alert Volume and Top Alerts widgets.

9. Add View widget and Name it "Utilization View", in Output Data Select Performance|Utilization|VM list. 

   ![image-20230328213541259](image-20230328213541259.png)

   

10. Add multiple View widgets to show performance views and edit the values to: 

- Name: cpu performance view -  Output Data: Performance|Utilization|VM CPU

![image-20230328210113992](image-20230328210113992.png)

- Name: guest memory Performance -  Output Data: Performance|Guest OS Memory

  <img src="image-20230328210608772.png" alt="image-20230328210608772" style="zoom:67%;" />

- Name: disk throughput performance  -  Output Data: Performance|Utilization|VM Disk Troughput (total)

<img src="image-20230328210753467.png" alt="image-20230328210753467" style="zoom:67%;" />

11. Add view widget, rename it to OS uptime and choose Output data: Availablity|Guest OS Uptime

![image-20230328211112779](image-20230328211112779.png)

12. Select view widget, name:Potential cost savings -  Object Data: Cost|VM Potential Savings

    ![image-20230328214707961](image-20230328214707961.png)

    13. Add Heatmap widget name it "workload and contention". For Output Data:

        - Configuration: load/contention

        - Name: load/contention

        - Group by: Virtual Machine 

        - Mode: General

        - Object Type: Virtual Machine 

        - Size by: CPU|Workload (%)

        - Color by: CPU|Contention(%)

          ![image-20230328215223151](image-20230328215223151.png)

          14. Add Object Relationship (Advanced) widget and rename it to Object

              ![image-20230328215423302](image-20230328215423302.png)15. Add Topology Graph widget and rename to Topo Graph 

              ![image-20230328215720675](image-20230328215720675.png)

Custom View

1. Go to View -> Manage Views

   ![image-20230328215953785](image-20230328215953785.png)

2. 
3. 

Interactions 

1. Go to Show Interactions tab

   ![image-20230328211241747](image-20230328211241747.png)

   2. Create interaction between Select your application widget and all the widgets on canvas 

      ![image-20230328221153371](image-20230328221153371.png)



3. Select Utilization List object and create interactions with listed widgets. 

   <img src="image-20230328221310534.png" alt="image-20230328221310534" style="zoom:50%;" />

   4. Save changes

      ![image-20230328221555472](image-20230328221555472.png)

      