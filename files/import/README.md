# Making your Workspace workable

- Click on **Extend** a couple of times to extend the time the Lab stays alive. 
- Close the Lab Manual by clicking **the X:**<img src="C:/Users/bgron/AppData/Roaming/Typora/typora-user-images/image-20230329190904711.png" alt="image-20230329190904711" style="zoom:67%;" />
  - Maximize the Lab window by clicking the **Maximize Icon**
    <img src="C:/Users/bgron/AppData/Roaming/Typora/typora-user-images/image-20230329191237802.png" alt="image-20230329191237802" style="zoom:50%;" />

## vSphere requisites

We need to tag some VM’s that we will use in our Lab to get some members of a Custom group, and use that group in dashboards and views:

- In vSphere, Click **the workload domain**, 
- click **VMs**
- **select** the 5 VMs as shown
- RightClick and Choose **Assign Tag** from the Tags & Custom Attributes
  <img src="./assets/image-20230329194444962.png" alt="image-20230329194444962" style="zoom:50%;" />

- Click **Yes** to confirm this action on 5 objects
- Click the Blue **Add Tag**
- Click **Create New Category**
- ​    Category Name: **appowner**
- ​    Click **Many Tags**
- ​    Click **Create**
- Under the Create Tag, use Name: **Kate**, and Category: **appowner**, then Click **Create**
  <img src="./assets/image-20230329195043889.png" alt="image-20230329195043889" style="zoom:50%;" />

Under the “5 objetcs - Assign Tag” window, Select the appropriate tag and click **Assign**

<img src="./assets/image-20230329195458264.png" alt="image-20230329195458264" style="zoom:50%;" />

Congratulations, we’re done with the vSphere portion  :-)

# Looking for Lab files

On the desktop, double-click **Lab Files** and browse to the location shown here. Just note the location of the folder and files, as they will be used in the import section below. 

- The first being the custom_groups

<img src="C:/Users/bgron/AppData/Roaming/Typora/typora-user-images/image-20230329191503597.png" alt="image-20230329191503597" style="zoom:50%;" />

# Import into Aria Operations

## Import a custom group

- Click **Environment**
- Click **Custom Groups**
- on the three dotted menu select **Import**
  ![image-20230329191855755](C:/Users/bgron/AppData/Roaming/Typora/typora-user-images/image-20230329191855755.png)

- Click **BROWSE…**
- Browse to the folder called **custom_groups**
- select the **Ops Exp Day - CustomGroup.json** file
- Click **Import** 
- after the import, click **Done**
  <img src="C:/Users/bgron/AppData/Roaming/Typora/typora-user-images/image-20230329192151847.png" alt="image-20230329192151847" style="zoom:50%;" />



## Importing a view

Goto Dashboards>Views and select **Manage Views**
<img src="C:/Users/bgron/AppData/Roaming/Typora/typora-user-images/image-20230329192340121.png" alt="image-20230329192340121" style="zoom:50%;" />

- In the views, on the dotted menu, choose **Import**

  <img src="C:/Users/bgron/AppData/Roaming/Typora/typora-user-images/image-20230329192500334.png" alt="image-20230329192500334" style="zoom:50%;" />

- Click Browse an go to the **views** subfolder 

- **select** the Zip file

- Click **Open**

  <img src="C:/Users/bgron/AppData/Roaming/Typora/typora-user-images/image-20230329192703704.png" alt="image-20230329192703704" style="zoom:50%;" />

  After you have imported Click **DONE**

<img src="C:/Users/bgron/AppData/Roaming/Typora/typora-user-images/image-20230329192750386.png" alt="image-20230329192750386" style="zoom:50%;" />

## Importing a dashboard

- Click **Dashboards**

- Select **Manage Dashboards**
  <img src="./assets/image-20230329192922904.png" alt="image-20230329192922904" style="zoom:50%;" />

- On the dotted menu, click **Import**
  <img src="./assets/image-20230329193149141.png" alt="image-20230329193149141" style="zoom:50%;" />

- We need to import <u>BOTH</u> these dashboards
- We will need to; Browse + Open **Twice**: 
  <img src="./assets/image-20230329193403927.png" alt="image-20230329193403927" style="zoom:50%;" />

- Repeat for the other dashboard

Now You’re done and ready for some real work  :-) 