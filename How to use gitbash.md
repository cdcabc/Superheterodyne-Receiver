Download link:
https://git-scm.com/downloads

After going through the process of installing it an icon like this should appear if you go searching for it in windows:
![[Pasted image 20250424000243.png]]
![[Pasted image 20250424000225.png]]

To make it so there is a common repo between us you want to make a folder on your desktop and name it anything
![[Pasted image 20250424000352.png]]
In the above my main folder for the project is Class Notes

Inside the folder right click and there should be a pop up with the first option being View. At the very bottom click the "Show more options button"

![[Pasted image 20250424000719.png]]
In the above you want to click "Git Bash Here" and it will bring up a terminal like below:
![[Pasted image 20250424000813.png]]

Inside of this terminal you want to write:
![[Pasted image 20250424000933.png]]

The https link comes from the Github repository that I created, this can be viewed by opening up the below link:
https://github.com/cdcabc/Superheterodyne-Receiver

This is the view you will see:
![[Pasted image 20250424001040.png]]

If you click on the green <Code> button it will display the below:
![[Pasted image 20250424001304.png]]

From there it will create a folder within your existing folder that will be named "Superheterodyne-Receiver"

Inside of that folder should be all the current notes that exist for the project currently.
![[Pasted image 20250424002001.png]]


Once you begin editing the notes or adding things of your own and you want to save them to the communal github, within the "Superheterodyne-Receiver" folder you want to open up a gitbash terminal within that folder.

Type git status and it will display all the changes you have made:
![[Pasted image 20250424002254.png]]


Next if you want add all changes type git add --all:
![[Pasted image 20250424002405.png]]
After doing this, retyping git status will display all the files you have staged for commit to be green text

Next you will want to commit them to the repo:
![[Pasted image 20250424002527.png]]
In the above git commit -m "" will allow you to push the notes with a message. The message is just nice to have since it will allow us to look back and see if something broke at this point (Imagining more for code than notes here tbh)

After this step you will want to type git push:
![[Pasted image 20250424002719.png]]

Next check the github to make sure that it all pushed correctly (Mostly just looking at the time stamp tbh):
![[Pasted image 20250424002801.png]]









