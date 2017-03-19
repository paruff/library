# Continuous Integration - Lab 05
## Jenkins

### GUI - web browser
1. In [Jenkins](http://dlsysadm-ap72:28080/jenkins/view/DevOps%204%20Teams%20View/)Create a "New Item" 
2. Enter and **Item Name** "commit-hello-{f_last}"
3. Select "Maven Project"
4. Click "OK"
5. Click "Restrict where this project can be run" 
6. Enter "Build_slave" into "Label Expression"
7. Select Source Code Management
8. Select **Git**
9. Enter Repository URL "ssh://git@dlv-sys-cm09:7999/devopsws/hello_world.git"
10. Select in the field "Credentials" , 07ujc4s (dev CM ID)
11. In **Build Triggers**, select **Poll SCM**
12. Deselect "Build whenever a SNAPSHOT dependency is built"
13. Enter "* * * * *" into **schedule**
14. In **Build**, enter "package -s settings.xml" into **Goals and options**
15. Select **E-mail Notification** in **Build Settings** and enter your email into the **Recipient** field.
16. Select **Save**
17. Select **Build Now**, on the left
18. Return to jenkins, click on your commit-hello- and now you should see a blue ball=Success next to a successful build. 
