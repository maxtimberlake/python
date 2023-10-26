<h1>Updating File permissions in Linux</h1>

<h2>Description</h2>
At my organization, the research team is tasked with revising the file permissions for specific files and directories within the projects directory. The current permissions don't align with the appropriate level of authorization. Verifying and adjusting these permissions is crucial for maintaining system security. To accomplish this, I undertook the following steps
<br />


<h2>Languages and Utilities Used</h2>

- <b>Python</b> 


<h2>Check file and directory details:</h2>


<p align="center">
The provided code showcases my utilization of Linux commands to ascertain the current permissions assigned to a particular directory within the file system
<br />
<br/>
<img src="https://imgur.com/GQDqLsY.png" height="80%" width="80%" alt="SQL_Lab"/>
<br />
<br />
The initial line in the screenshot exhibits the command I inputted, while the subsequent lines exhibit the resulting output. The code enumerates all the items within the projects directory. I employed the ls command with the -la flag to present a comprehensive listing of the file contents, including those that are hidden. The outcome of my command reveals the presence of a directory labeled 'drafts,' a concealed file named '.project_x.txt,' and an additional five project files. The 10-character sequence in the initial column signifies the permissions allocated to each file or directory
<br />
<br />


<h2>Change file permissions:</h2>


<p align="center">
The organization decided that 'other' users should not possess write access to any of their files. In adherence to this, I consulted the previously retrieved file permissions. I concluded that 'project_k.txt' needed to have write access revoked for 'other' users. The provided code illustrates the Linux commands I employed to execute this task
<br />
<br /> 
<img src="https://imgur.com/4UhSBhe.png" height="80%" width="80%" alt="SQL"/>
<br />
<br />
The initial two lines in the screenshot showcase the commands I inputted, while the subsequent lines exhibit the output of the second command. The 'chmod' command is responsible for altering permissions on files and directories. The initial argument designates which permissions are to be modified, and the second argument specifies the targeted file or directory. In this instance, I revoked write permissions from 'other' for the 'project_k.txt' file. Following this, I employed 'ls -la' to inspect the modifications I implemented.
<br />
<br />

<h2>Change file permissions on a hidden file:</h2>


<p align="center">
The research team at my organization recently moved 'project_x.txt' to an archive. They wish to restrict write access to this project while allowing both the user and group to retain read access.The provided code showcases how I utilized Linux commands to modify the permissions:
<br />
<br /> 
<img src="https://imgur.com/3Q3ee48.png" height="80%" width="80%" alt="SQL"/>
<br />
<br />
In the provided screenshot, the first two lines display the commands I entered, while the subsequent lines show the output of the second command. I recognized '.project_x.txt' as a hidden file due to its leading period (.). In this example, I executed a series of actions: I removed write permissions from both the user and group using 'u-w'. Following that, I revoked write permissions from the group with 'g-w' and granted read permissions to the group using 'g+r'.
<br />
<br />


<h2>Change directory permissions:</h2>


<p align="center">
My organization has specified that only the 'researcher2' user should have access to the 'drafts' directory and its contents. This implies that no one aside from 'researcher2' should possess execute permissions.The provided code illustrates how I employed Linux commands to implement these changes::<br/>
<br />
<br />
<img src="https://imgur.com/xvlSK45.png" height="80%" width="80%" alt="SQL"/>
<br/>
<br/>
The initial two lines in the screenshot showcase the commands I inputted, while the subsequent lines present the output of the second command. I had previously established that the group held execute permissions. Consequently, I utilized the 'chmod' command to eliminate them. It was unnecessary to add execute permissions for the 'researcher2' user, as they already had them.
<br />
<br />
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
