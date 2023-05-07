Download Link: https://assignmentchef.com/product/solved-mtrn4230-group-project
<br>
This group project is about designing of a pick and place robot manipulator in a simulated environment. Every group/team has seven people involved. The instruction about forming group has been shared in MS Teams <em>Files/General/GroupProject/GroupProjectMTRN4230.mp4</em>.

This document outlines the important aspect of this project as well as due dates, marking criteria and deliverables.

<h1>Problem description</h1>

One of the typical applications for robot arms is performing pick and place tasks in various industrial setups. It involves

<ol>

 <li>Detection of an object based on sensor information.</li>

 <li>Using proper gripper for a robot arm.</li>

 <li>Actuation of a robot arm towards the target and picking the object</li>

 <li>Moving to the pre-determined destination location to place the object</li>

 <li>Placing the object at the destination location</li>

</ol>

Many components of the above task are adjustable; and based on the type of the object or complexity of the environment, this task can be easy or difficult.

Let us consider an automated warehouse as pharmaceutical product distribution centre (DC) that has automated order and fulfilment systems. The pickers (people or technology used to pick items and collect them to fulfil the order) are robot arms programmed for the pick and place tasks.  This warehouse as a modern DC ensures, small orders are processed as fast as possible and the next day delivery is guaranteed for their customers. These commitments make the warehouse very dependant to the automation. Robot pickers are part of warehouse control system (WCS).

Chemists, as the main customers, order the products in small amounts and the next day delivery ensures products are delivered to them on time. This encourages them to order less but more frequent. It reduces the cost of stock accumulation/maintenance and improves the diversity of the products on the shelves without losing serviceability.

How an order is fulfilled

Orders are not coming in bulk but in a smaller amount. So, it means DC needs to operate as a retailer but with a broad range of orders and huge numbers. With all the planning still order fulfilment / picking the products in small amounts and diverse profile is a challenge. The way the stock is maintained in the warehouse is done by warehouse management system (WMS). WMS uses various methods and algorithms to club products and pre-order bulk amounts of them to maintain and replenish the warehouse at the same time WMS ensures the customer orders can be fulfilled based on stock in hand, then the orders are sent to WCS for fulfilment.

One of the approaches WMS/WCS uses is: mixing products in one container to reduce waste of storage capacity i.e. mix tote with dividers. It means one container or tote can hold three products at the same time shown in Figure 1 and it is the responsibility of the picker to pick from a correct section within a tote based on the order details provided.




<em>Figure 1 Tote with dividers (https://www.alibaba.com/product-detail/Industrial-Plastic-Storage-Tote-Binswith_60631536472.html) </em>

Regarding the storage of mix totes, an automated storage and retrieval system is used to store and retrieve totes from the racks as shown in Figure 2. The totes to be stored are fed either from the decant lines or totes that already used to pick items from. Retrievals are done to send totes to robot pickers to fulfil the orders.




<em>Figure 2 Rack storage system (</em><a href="https://www.interlakemecalux.com/warehouse-logistics-videos/miniload-automated-warehouse-boxes"><em>https://www.interlakemecalux.com/warehouse</em></a><a href="https://www.interlakemecalux.com/warehouse-logistics-videos/miniload-automated-warehouse-boxes"><em>–</em></a><a href="https://www.interlakemecalux.com/warehouse-logistics-videos/miniload-automated-warehouse-boxes"><em>logistics</em></a><a href="https://www.interlakemecalux.com/warehouse-logistics-videos/miniload-automated-warehouse-boxes"><em>–</em></a><a href="https://www.interlakemecalux.com/warehouse-logistics-videos/miniload-automated-warehouse-boxes"><em>videos/miniload</em></a><a href="https://www.interlakemecalux.com/warehouse-logistics-videos/miniload-automated-warehouse-boxes"><em>–</em></a><a href="https://www.interlakemecalux.com/warehouse-logistics-videos/miniload-automated-warehouse-boxes"><em>automated</em></a><a href="https://www.interlakemecalux.com/warehouse-logistics-videos/miniload-automated-warehouse-boxes"><em>warehouse</em></a><a href="https://www.interlakemecalux.com/warehouse-logistics-videos/miniload-automated-warehouse-boxes"><em>–</em></a><a href="https://www.interlakemecalux.com/warehouse-logistics-videos/miniload-automated-warehouse-boxes"><em>boxes</em></a><a href="https://www.interlakemecalux.com/warehouse-logistics-videos/miniload-automated-warehouse-boxes"><em>)</em></a>

Picker robots

Picker robots are used as shown in Figure 3 in an illustrative setup. The robot receives a tote containing products, it picks items based on the order details sent to the robot and places them in another container that finally will be shipped to the customer.




<em>Figure 3 picker robot arm (https://www.roboticstomorrow.com/images/articles/12618.jpg) </em>

As shown in Figure 3, the robot uses a vision system to identify the item e.g. yellow box need to be picked. The gripper is actuated, and specific number of yellow items are picked based on the command from WCS.




<h1>Task outline</h1>

<ol>

 <li>Research about the implementation of pick and place task by a robot arm and software architecture of such a system</li>

</ol>

o It is expected that the team first comes up with a design by doing some research. It is important to decide about the main structure of your codebase, the algorithm, and main components. You can use the information in this document and information shared with you during the tutorial to find your path. The goad is: you come up with ideas! It can be very simplified or very complex.

<ol>

 <li>The pick and place task should be done by MATLAB/Simulink and ROS as the minimum requirement. If you would like to do it fully in ROS it is okay. However, the programming language in ROS should be Python.</li>

 <li><strong>You do not need to have a complex simulation. The minimum requirement is defined here: </strong>

  <ul>

   <li>One robot arm UR5</li>

   <li>One RGB-D camera (Kinect)</li>

   <li>Picking stationary objects (not moving objects)</li>

   <li>Detection of objects based on classifier and/or image processing techniques</li>

   <li>Detection of objects based on shape of the object</li>

   <li>Detection of objects based on colour of the object</li>

   <li>Detection of objects based on colour and shaper of the object</li>

   <li>Using depth data from RGB-D (Kinect) in the pick and place task</li>

   <li>Location of objects before pick should be randomised when the program starts but the shape and colours are pre-determined</li>

   <li>Minimum 10 objects need to be picked and placed</li>

   <li>Text-based or the graphic user interface to o select number of picks robot need to do and o option to select colour and/or shape of the objects to pick as the goal</li>

   <li>Robot movements should be based on online information coming from simulation and calculated not pre-defined or pre-determined movements or path. Only one predefined HOME position is allowed and the destination for placing the order is pre-determined</li>

  </ul></li>

 <li>Formulate forward and inverse kinematics in MATLAB for the robot arm</li>

 <li>Trajectory planning for robot manipulator</li>

 <li>Design of object detector with a classifier based on RGB and depth data (RGB-D sensor)</li>

 <li>Completing the design of the simulation platform in ROS as an external simulator using a</li>

</ol>

UR5 robot o ROS is used to create an external simulator. Ros is supplied as virtual matching with basic component, so no need to install ROS or initialise the environment. However, the provided model components and controllers need to be updated to cater for the pick and place task. No Python or C++ programming in ROS is expected/required however models in Gazebo need to be added/updated to support your design using Unified Robotic Description Format (URDF) that is an XML file format.

<strong>Note:</strong> Gripper model and gripper controller are not provided. It is expected that the team selects a gripper and sets up a controller in ROS however no need to create a gripper from scratch, using existing models (can be found online) is allowed to minimise programming in ROS. The gripper type can be a suction or fingers or any other type depending on the design you will decide.

<ol start="6">

 <li>Simulate pick and place task. o Simulation software MATLAB/Simulink and ROS are used</li>

 <li>Teamwork and workload distribution

  <ul>

   <li>teamwork and continuous communication among group members matter and it is pre-requirement for marking o Use your MS Team group for communication instead of emails to have a good track of team interactions. It is needed for marking and tracking purpose</li>

   <li>fair workload distribution o Team needs to show how every team member is actively helping the team has a task and is sharing part of the load in a fair manner</li>

  </ul></li>

</ol>

<strong>Note</strong> This semester most of us did not have opportunity to meet and team up. We do not have the opportunity to find right people for our team and select our teammates. However, we can show the way we utilise tools and available resources in a smart way to compensate for the physical distance. In addition, it’s a typical example of the real-life that we cannot always select our teammates, e.g. you join a company with an existing team, we can practice how to make most of it based on what we know and what we have.

<ol start="8">

 <li>Project management o There is no expectation for comprehensive project management since it is not project management course, however, it is expected that teams are following a path and is mindful of the deadline and the progress with the basic planning and tracking tools or documents, for example, teams need to have

  <ul>

   <li>Project Gantt chart</li>

   <li>Project planning and task allocation</li>

   <li>Budgeting time and resources</li>

  </ul></li>

</ol>




Checkpoints and deliverables










<h1>How to use Prepared ROS Kinetic Environment</h1>

If you want to avoid setting up your environment, you may start using the VM shared with you to speed up. Some of the main packages.

<ul>

 <li>Ros Kinetic <a href="http://wiki.ros.org/kinetic/Installation/Ubuntu">[</a><a href="http://wiki.ros.org/kinetic/Installation/Ubuntu">http://wiki.ros.org/kinetic/Installation/Ubuntu</a><a href="http://wiki.ros.org/kinetic/Installation/Ubuntu">]</a></li>

 <li>Catkin [<a href="http://docs.ros.org/melodic/api/catkin/html/user_guide/installation.html">http://docs.ros.org/melodic/api/catkin/html/user_guide/installation.html</a><a href="http://docs.ros.org/melodic/api/catkin/html/user_guide/installation.html">]</a></li>

 <li>MoveIt [<a href="https://moveit.ros.org/install/">https://moveit.ros.org/install/</a><a href="https://moveit.ros.org/install/">]</a></li>

 <li>Universal Robot [<a href="https://github.com/ros-industrial/universal_robot">https://github.com/ros</a><a href="https://github.com/ros-industrial/universal_robot">–</a><a href="https://github.com/ros-industrial/universal_robot">industrial/universal_robot</a><a href="https://github.com/ros-industrial/universal_robot">]</a></li>

 <li>Ur5_ROS-Gazebo [<a href="https://github.com/lihuang3/ur5_ROS-Gazebo">https://github.com/lihuang3/ur5_ROS</a><a href="https://github.com/lihuang3/ur5_ROS-Gazebo">–</a><a href="https://github.com/lihuang3/ur5_ROS-Gazebo">Gazebo</a><a href="https://github.com/lihuang3/ur5_ROS-Gazebo">]</a></li>

</ul>




What is ROS

<table width="577">

 <tbody>

  <tr>

   <td width="577">“The Robot Operating System (ROS) is a set of software libraries and tools that help you build robot applications. From drivers to state-of-the-art algorithms, and with powerful developer tools, ROS has what you need for your next robotics project. And it’s all open source.” [ros.org]</td>

  </tr>

  <tr>

   <td width="577"></td>

  </tr>

 </tbody>

</table>




Run the setup

<table width="601">

 <tbody>

  <tr>

   <td width="601">VirtualBox-5.2.22-126460-Win.exe</td>

  </tr>

  <tr>

   <td width="601"> </td>

  </tr>

 </tbody>

</table>




How to import image in virtual box




<table width="601">

 <tbody>

  <tr>

   <td width="601"> </td>

  </tr>

  <tr>

   <td width="601"></td>

  </tr>

  <tr>

   <td width="601"> </td>

  </tr>

  <tr>

   <td width="601">Username Javad Password 777</td>

  </tr>

 </tbody>

</table>




Install Virtual Box Guest Additions




<table width="553">

 <tbody>

  <tr>

   <td width="553"></td>

  </tr>

  <tr>

   <td width="553"> </td>

  </tr>

  <tr>

   <td width="553"></td>

  </tr>

 </tbody>

</table>




<table width="553">

 <tbody>

  <tr>

   <td width="553"> </td>

  </tr>

  <tr>

   <td width="553"></td>

  </tr>

 </tbody>

</table>




See some actions





