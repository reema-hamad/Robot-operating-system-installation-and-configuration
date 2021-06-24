# ROS تثبيت وتشغيل باكج الذراع على نظام


1-  VirtualBox نقوم في تثبيت 

* هنا من خلال الرابط تقوم بإختيار النظام المناسب لجهازك 
 
  https://www.virtualbox.org/wiki/Downloads   

2-  ubuntu-desktop كما ايضا قمت بتحميل للأصدار (16.04.7 )

      https://releases.ubuntu.com/16.04/ 


##   VirtualBox داخل تطبيق  

1.  قمت بفتح ملف جديد حيث وضعت الأسم ثم اخترت المساحة الجيده للتخزين 
 1.  قمت بتثبيت الاوبنتو داخل الملف الذي انشأته  في الفيرجوال  
 1. Browser بعد تثبيت الاوبنتو نبدأ بالعمل عليه ثم ندخل الى 
 1. s-m.com.sa/ros.txt نقوم بالبحث عن هذه  الاوامر التي تستخدم لتثبيت باكج اداة الروز يوجد الكثير غير هذه الصفحة لكن لاحظت ان هذه الأوامراوضح واسهل للمستخدمين المبتدئين 
 1. Terminal بعد ذلك نقوم بالدخول على 
1. التى استخرجناها من المتصفح  Ros commands ثم نقوم بكتابة 
![Untitled](https://user-images.githubusercontent.com/85697922/123289349-12b9d780-d519-11eb-89aa-77fb4a9521a0.png)

سوف تظهر لنا الذراع بهذا الشكل
![Untitled1](https://user-images.githubusercontent.com/85697922/123289720-5f9dae00-d519-11eb-9fe8-973445e31e03.png)

##  gazebo عندما نتنهي نقوم بفتح   

 ###  :  من خلال اربع خطوات


   : الخطوة الاولى
   
نقوم بفتح 

New Terminal 

roslaunch robot_arm_pkg check_motors.launch ثم نقوم بكتابة هذا الأمر 
Rviz هنا سوف تظهر ويوجد داخلها الذراع باللون الاحمر ايضا منيو للتحكم بالذراع وتحريكة 


الخطوة الثانية : 
 
نقوم بفتح 

New Terminal 

roslaunch robot_arm_pkg check_motors_gazebo.launch ثم نقوم بكتابة هذا الأمر

gazebo هنا سوف نشاهد الواجهة الخاصه بـ 

Rviz  تحتوي على ذراع لونه رمادي نفس شكل الذراع الموجود في  
 لكن بإختلاف اللون والواجهه
 
 
 الخطوة الثالثة : 
 
 نقوم بفتح 

New Terminal 

directory  هنا سوف نقوم بالدخول  الى  
من اجل تغيير الصلاحيات 
cd catkin_ws/src/arduino_robot_arm/robot_arm_pkg/scripts هنا قمنا بالدخول 

sudo chmod +x joint_states_to_gazebo.py هنا اعطينا أمر بتغيير الصلاحية 


### chmod هو أمر تغيير الصلاحيات

 
الخطوة الرابعة والأخيرة : 

نقوم بفتح 
New Terminal 

ثم نضع هذا الأمر  
rosrun robot_arm_pkg check_motors_gazebo.launch  

الان عندما نقوم بتحريك الذراع من القائمه الموجودة سوف يتحرك كلا من الذراعين  الموجودات في  الــ 
gazebo  &  Rviz 
 

https://user-images.githubusercontent.com/85697922/123289894-82c85d80-d519-11eb-8e61-5621148e052f.mp4



