---
layout: about
# image: /assets/img/blog/hydejack-9.jpg
description: >
  Jaehyun Shim's personal webpage.
hide_description: true
redirect_from:
  - /download/
---

<style>
  .btn {
    background-color: white;
    border: 1px solid gray;
    color: black;
    padding: 10px 20px;
    cursor: pointer;
    transition: transform 0.2s ease-in-out; /* Added transition property */
  }

  .btn.active {
    background-color: gray;
    color: white;
    transform: scale(1.1); /* Added transform property to enlarge the button */
  }
</style>

<div id="options" class="btn-group">
  <button class="btn active" data-tag="all">All</button>
  <button class="btn" data-tag="2013">2013</button>
  <button class="btn" data-tag="2015">2015</button>
  <!-- <button class="btn" data-tag="2017">2017</button> -->
  <button class="btn" data-tag="2018">2018</button>
  <button class="btn" data-tag="2019">2019</button>
  <button class="btn" data-tag="2020">2020</button>
  <button class="btn" data-tag="2021">2021</button>
  <button class="btn" data-tag="2022">2022</button>
</div>

<script>
  var buttons = document.getElementsByClassName("btn");
  var items = document.getElementsByClassName("item");

  for (var i = 0; i < buttons.length; i++) {
    buttons[i].addEventListener("click", function() {
      var current = document.getElementsByClassName("active");
      current[0].className = current[0].className.replace(" active", "");
      this.className += " active";
      
      var tag = this.getAttribute("data-tag");
      
      for (var j = 0; j < items.length; j++) {
        if (tag == "all" || items[j].getAttribute("data-tag") == tag) {
          items[j].style.display = "block";
        } else {
          items[j].style.display = "none";
        }
      }
    });
  }
</script>
<br>

<div id="items">

  <!-- 2022 ANYmal Stair Climbing -->
  <div class="item" data-tag="2022">
    <table style="width:100%;">
      <tr>
        <td style="width:50%; padding-right: 10px; min-height: 300px;">
          <img src="../assets/img/jaehyun/2022_anymal_stair_climbing.gif" style="width:100%; margin-bottom:1%;">
        </td>
        <td style="width:50%; vertical-align:top; font-size: 14px;">
          <b>ANYmal Stair Climbing</b>
          <br><br>
          In Edinburgh, most of my time was spent on ANYmal stair climbing for the Memory of Motion (Memmo) project. The GIF on the left was recorded on Sunday 4am...
          <br><br>
          Research <a href="../research">[Link]</a><br>
          Perceptive Locomotion Video <a href="https://youtu.be/W4HHLMNbcXo">[Link]</a><br>
        </td>
      </tr>
    </table>
  </div>

  <!-- 2022 Talos State Estimation -->
  <div class="item" data-tag="2022">
    <table style="width:100%;">
      <tr>
        <td style="width:65%; vertical-align:top; font-size: 14px;">
          <b>Talos State Estimation</b>
          <br><br>
          I developed Vicon state estimation integration for Talos. The proprioceptive state estimation couldn't give accurate estimates of the current pose, so I used the robot_localization package to fuse ground truth measurements from Vicon into it. The same problem occurred with ANYmal when it jumped, so I also used this integration to resolve the problem. Additionally, I collaborated on deploying a Centroidal Dynamics motion planner on the real Talos robot and developed ROS integration for it.
          <br><br>
          Robot Localization Wiki <a href="http://docs.ros.org/en/noetic/api/robot_localization/html/index.html">[Link]</a>
        </td>
        <td style="width:35%; padding-right: 10px; min-height: 300px;">
          <img src="../assets/img/jaehyun/2022_talos_hand_waving.gif" style="width:100%; margin-bottom:1%;">
          <img src="../assets/img/jaehyun/2022_talos_state_estimation.gif" style="width:100%; margin-bottom:1%;">
        </td>
      </tr>
    </table>
  </div>

  <!-- 2022 Kawada Nextage -->
  <div class="item" data-tag="2022">
    <table style="width:100%;">
      <tr>
        <td style="width:40%; padding-right: 10px; min-height: 300px;">
          <img src="../assets/img/jaehyun/2022_kawada_nextage.jpg" style="width:100%;">
        </td>
        <td style="width:60%; vertical-align:top; font-size: 14px;">
          <b>Kawada Nextage</b>
          <br><br>
          I did many tasks for the Nextage robot, including manual writing, maintenance, giving robot usage tutorials to lab members, and providing feedback on the Kawada project.
          <br><br>
          Pic taken on the last day of work.
        </td>
      </tr>
    </table>
  </div>

  <!-- 2022 ODRI Solo -->
  <div class="item" data-tag="2022">
    <table style="width:100%;">
      <tr>
        <td style="width:60%; vertical-align:top; font-size: 14px;">
          <b>ODRI Solo</b>
          <br><br>
          Solo was designed and developed by the Open Dynamic Robot Initiative (ODRI). For the use of the robot within the lab, I created a software framework and feedforward PD controller of this robot.
          <br><br>
          ODRI Solo <a href="https://open-dynamic-robot-initiative.github.io/">[Link]</a>
        </td>
        <td style="width:40%; padding-right: 10px; min-height: 300px;">
          <img src="../assets/img/jaehyun/2022_odri_solo.png" style="width:100%;">
        </td>
      </tr>
    </table>
  </div>

  <!-- 2021 ZIPGAEMI -->
  <div class="item" data-tag="2021">
    <table style="width:100%;">
      <tr>
        <td style="width:50%; padding-right: 10px; min-height: 300px;">
          <img src="../assets/img/jaehyun/2021_zipgaemi.gif" style="width:100%;">
        </td>
        <td style="width:50%; vertical-align:top; font-size: 14px;">
          <b>ZIPGAEMI, an indoor delivery robot</b>
          <br><br>
          I participated in the development of 'ZIPGAEMI', a wheeled mobile manipulator robot designed for indoor delivery purposes. It was a large team project that enabled the robot to navigate, detect elevator buttons, ride elevators, and deliver amenities to customers' rooms. Specifically, I took charge of the development of the software framework for the wheeled base.
          <br><br>
          It was my final project at ROBOTIS and I finally finished my long military replacement service.
          <br><br>
          Full Video <a href="https://youtu.be/6leVDb6EHi4">[Link]</a><br>
        </td>
      </tr>
    </table>
  </div>

  <!-- 2021 VSCode ROS2 -->
  <div class="item" data-tag="2021">
    <table style="width:100%;">
      <tr>
        <td style="width:40%; vertical-align:top; font-size: 14px;">
          <b>VSCode ROS2 Extension</b>
          <br><br>
          I've developed a ROS2 snippet extension to simplify ROS2 programming. At the time of writing this article, nearly 10,000 users are using it. Also the extension I made for ROS1 reached over 10,000 users a while back.
          <br><br>
          ROS VSCode Extension <a href="https://marketplace.visualstudio.com/items?itemName=JaehyunShim.vscode-ros">[Link]</a><br>
          ROS2 VSCode Extension <a href="https://marketplace.visualstudio.com/items?itemName=JaehyunShim.vscode-ros2">[Link]</a>
        </td>
        <td style="width:60%; padding-right: 10px; min-height: 300px;">
          <img src="../assets/img/jaehyun/2021_vscode_ros2.gif" style="width:100%;">
        </td>
      </tr>
    </table>
  </div>

  <!-- 2020 Generic Software Framework for Legged Robots -->
  <div class="item" data-tag="2020">
    <table style="width:100%;">
      <tr>
        <td style="width:60%; padding-right: 10px; min-height: 300px;">
          <img src="../assets/img/jaehyun/2020_generic_software_framework_for_legged_robots.gif" style="width:100%;">
        </td>
        <td style="width:40%; vertical-align:top; font-size: 14px;">
          <b>Generic Software Framework for Legged Robots</b>
          <br><br>
          As a side project, I created a generic software framework for legged robots using the ROS Control library. I made both ROS and ROS2 versions, and I even made a setup assistant using Qt. This was a spin-off project from a previous project I participated in. I am deeply grateful to all the members of the group who I met there and exchanged ideas with every Friday night.
          <br><br>
          Group Youtube Channel <a href="https://www.youtube.com/@dynamics5776/videos">[Link]</a><br>
        </td>
      </tr>
    </table>
  </div>

  <!-- 2019 OpenSource Robots -->
  <div class="item" data-tag="2019">
    <table style="width:100%;">
      <tr>
        <td style="width:50%; vertical-align:top; font-size: 14px;">
          <b>OpenSource Robots</b>
          <br><br>
          During my time at ROBOTIS, I had the opportunity to work on open-source projects including Turtlebot3, OpenManipulator, RH Gripper, and Dynamixel. I utilized many software tools and libraries and was involved in the development of software architecture, demos, GUI, performance checks, and CI/CD. It was a valuable experience to contribute to the ROS community by holding hackathons and ensuring seamless communication with users.
          <br><br>
          ROBOTIS OpenSource Robot <a href="https://emanual.robotis.com/docs/en/platform/">[Link]</a><br>
          ROBOTIS Github <a href="https://github.com/ROBOTIS-GIT">[Link]</a><br>
        </td>
        <td style="width:50%; padding-right: 10px; min-height: 300px;">
          <table style="width:100%; height:100%;">
            <tr>
              <td style="width:50%; height:50%; padding: 1px;">
                <img src="../assets/img/jaehyun/2019_om_p.gif" style="width:100%; height:100%;">
              </td>
              <td style="width:50%; height:50%; padding: 1px;">
                <img src="../assets/img/jaehyun/2019_om_x.gif" style="width:100%; height:100%;">
              </td>
            </tr>
            <tr>
              <td style="width:50%; height:50%; padding: 1px;">
                <img src="../assets/img/jaehyun/2019_gripper.gif" style="width:100%; height:100%;">
              </td>
              <td style="width:50%; height:50%; padding: 1px;">
                <img src="../assets/img/jaehyun/2019_tb3.gif" style="width:100%; height:100%;">
              </td>
            </tr>
          </table>
        </td>
      </tr>
    </table>
  </div>

  <!-- 2018 OM Friends -->
  <div class="item" data-tag="2018">
    <table style="width:100%;">
      <tr>
        <td style="width:50%; padding-right: 10px; min-height: 300px;">
          <table style="width:100%; height:100%;">
            <tr>
              <td style="width:50%; height:50%; padding: 1px;">
                <img src="../assets/img/jaehyun/2018_om_stewart.gif" style="width:100%; height:100%;">
              </td>
              <td style="width:50%; height:50%; padding: 1px;">
                <img src="../assets/img/jaehyun/2018_om_delta.gif" style="width:100%; height:100%;">
              </td>
            </tr>
            <tr>
              <td style="width:50%; height:50%; padding: 1px;">
                <img src="../assets/img/jaehyun/2018_om_planar.gif" style="width:100%; height:100%;">
              </td>
              <td style="width:50%; height:50%; padding: 1px;">
                <img src="../assets/img/jaehyun/2018_om_linear.gif" style="width:100%; height:100%;">
              </td>
            </tr>
          </table>
        </td>
        <td style="width:50%; vertical-align:top; font-size: 14px;">
          <b>OpenManipulator Friends</b>
          <br><br>
          I joined ROBOTIS in Korea and worked on OpenManipulator Friends, which are open-source, customizable, small-sized serial and parallel manipulators including Stewart, Delta, Planar, Linear, and SCARA. My work involved modifying existing hardware designs using Onshape, 3D printing, assembling the parts, implementing forward and inverse kinematics, and brainstorming demo ideas. It was a challenging experience with many 9-to-9 work days, but it was also very rewarding with unforgettable moments of joy when every demo video was released.
          <br><br>
          OpenManipulator Friends <a href="https://emanual.robotis.com/docs/en/platform/openmanipulator_x/friends/#friends">[Link]</a><br>
        </td>
      </tr>
    </table>
  </div>

  <!-- 2017 Grad School -->
  <!-- <div class="item" data-tag="2017">
    <table style="width:100%;">
      <tr>
        <td style="width:50%; padding-right: 10px; min-height: 300px;">
          <img src="../assets/img/jaehyun/placeholder.gif" style="width:100%;">
        </td>
        <td style="width:50%; vertical-align:top; font-size: 14px;">
          대학원 연구 영상
        </td>
      </tr>
    </table>
  </div> -->

  <!-- 2015 PR2 Lab Introduction -->
  <div class="item" data-tag="2015">
    <table style="width:100%;">
      <tr>
        <td style="width:70%; vertical-align:top; font-size: 14px;">
          <b>PR2 Lab Introduction</b>
          <br><br>
          I did a five-month internship in Shenzhen. I had the opportunity to work on robot control with PR2 for the first time. During my internship, I acquired C++, Python, and ROS (Robot Operating System) skills. At the end of the internship, I developed a demo that the robot navigating around the lab while introducing the lab and the robot itself.
          <br><br>
          Used libraries: mapping, navigation, joint control, and sound play
        </td>
        <td style="width:30%; padding-right: 10px; min-height: 300px;">
          <img src="../assets/img/jaehyun/2015_pr2_lab_introduction.gif" style="width:100%;">
        </td>
      </tr>
    </table>
  </div>

  <!-- 2015 University of Tokyo -->
  <!-- <div class="item" data-tag="2015">
    <table style="width:100%;">
      <tr>
        <td style="width:50%; padding-right: 10px; min-height: 300px;">
          <img src="../assets/img/jaehyun/placeholder.gif" style="width:100%;">
        </td>
        <td style="width:50%; vertical-align:top; font-size: 14px;">
          프로젝트, 연구 영상
        </td>
      </tr>
    </table>
  </div> -->

  <!-- 2013 Hand Detection -->
  <div class="item" data-tag="2013">
    <table style="width:100%;">
      <tr>
        <td style="width:50%; padding-right: 10px; min-height: 300px;">
          <img src="../assets/img/jaehyun/2013_hand_detection.gif" style="width:100%;">
        </td>
        <td style="width:50%; vertical-align:top; font-size: 14px;">
          <b>Hand Detection</b>
          <br><br>
          During my 2nd and 3rd years of uni, all I can recall is developing, developing, and more developing. In one project, I created a virtual hand using OpenGL and programmed it to imitate the hand movements detected using OpenCV.
          <br><br>
          After the Battleship competition, I ended up in 2nd place once again :)
        </td>
      </tr>
    </table>
  </div>

  <!-- 2013 Robot Hand Control -->
  <div class="item" data-tag="2013">
    <table style="width:100%;">
      <tr>
        <td style="width:50%; vertical-align:top; font-size: 14px;">
          <b>Robot Hand</b>
          <br><br>
          I was up for three nights straight, designing finger structures, cutting aluminium plates, drilling holes, and assembling them. But, during the demonstration, the gears ended up breaking.
          <br><br>
          It was clearly a student-level project, but it was a great fun to work on. And I miss so much the yakisoba and 100 yen chicken I ate while working late at night...
        </td>
        <td style="width:50%; padding-right: 10px; min-height: 300px;">
          <img src="../assets/img/jaehyun/2013_robot_hand_control.gif" style="width:100%;">
        </td>
      </tr>
    </table>
  </div>
</div>
