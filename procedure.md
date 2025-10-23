## **---------------Procedural commands for the web page development--------------**



#### **(Note: "#" refers to commands do not copy "#")**





1. **First launch an instance through EC2 service in AWS.**

   
2. ##### **Second create a folder and create maven project using the commands by providing project name.**

######  
          # mvn archetype:generate                               (this command is used to initialize to build the maven project)

 ###### **After using the command choose web project by choosing the particular number (EX:2292) and provide all the details according to project.**





##### **3. Next once the maven project is created then open the folder in VS code and work on the project by adding code like HTML or by adding any other files.**

##### 

##### **4. Then push the code to the GitHub repository through VS code.**

##### 

##### **5. After that open the Gitbash and paste the SSH that is obtained through the instance after that add these commands.**

##### 

##### **6. To change the user to root user**

###### 
            # sudo su -



##### **7. To update the server or repo**

###### 
           # apt update



##### **8. To install tomcat 9.0**

###### 
          # wget https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.111/bin/apache-tomcat-9.0.111.tar.gz



##### **9. To install java**

###### 
         # apt install openjdk-17-jre-headless -y



##### **10. Add the tar file**

###### 
        # tar -zxvf apache-tomcat-9.0.111.tar.gz



##### **11. To remove the tar.gz file**

###### 
        # rm -rf apache-tomcat-9.0.111.tar.gz



##### **12. Enter inside the tomcat file**

###### 
        # cd apache-tomcat-9.0.111/



##### **13. Check the files or sub files**
######   
         # ls
         # cd    (use this command after ls in order come outside the sub files)



##### **14. Insert the additional commands inside xml so first use this command**

###### 
         # vi apache-tomcat-9.0.111/conf/tomcat-users.xml

###### **(after this command click i and under the rollback add this command)**

###### **#
           <role rolename="manager-gui"/>
           <role rolename="manager-script"/>
           <role rolename="manager-jmx"/>
           <role rolename="manager-status"/>
           <user username="admin" password="admin" roles="manager-gui, manager-script, manager-jmx, manager-status"/>


##### **15. To configure webapps** 

###### 
          # vi apache-tomcat-9.0.111/webapps/manager/META-INF/context.xml

###### **(after this comment click i and comment cookie line 3 lines from cookie statement)**



##### **16. After this clone the project by pasting the repository url**

###### 
         # git clone "paste the repository url"



##### **17. Go inside the repository or inside the project**

###### 
         # cd "repository name/"



##### **18. And type this**

###### 
         # pwd



##### **19. After that use this command**

###### 
         # mvn clean package



##### **20. If the maven is not installed then you have to install maven use**

###### 
         # apt install maven



##### **21. Check the version if maven is installed**

###### 
         # mvn --version



##### **22. After that go inside the repo or project**

###### 
         # cd "repo name/"



##### **23. Use this command**

###### 
        # mvn clean package



##### **24. Get outside the project files using**

###### 
        # cd ..



##### **25. Copy the files using**

###### 
        # cp "repo name"/target/"repo file.war" apache-tomcat-9.0.111/webapps/



##### **26. Add the startup file command to start the tomcat**

###### 
        # sh apache-tomcat-9.0.111/bin/startup.sh



##### **27. If any changes is made then you have to pull the code so make changes and push the code in VS code after that use this commands one by one **

###### 
         # cd "repo name"/                                                              (use this to get inside the repo or project)**

###### 
         # git pull origin main                                                         (to pull the code to remote repo)**

###### 
         # mvn clean package                                                            (again use this command to build the package)**

###### 
         # cp "repo name"/target/"repo file.war" apache-tomcat-9.0.111/webapps/         (copy the files again)**

###### 
         # sh apache-tomcat-9.0.111/bin/startup.sh                                      (start the server again)**



##### **28. Now the code will be pulled to remote repo and changes made will be shown/visible**



