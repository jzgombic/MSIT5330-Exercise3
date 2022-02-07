
Exercise 3
Use pdf format for all homework submissions (not word document format)
1
Create a new github repository (you will need to create a personal access token). Commit the
Jenkinsfile from the lecture notes to the master (default) branch. It will run the shell command:
"echo this is the master branch".
Create a new branch called "testing", and modify the Jenkins file in that branch. It will run the
command "echo this is a testing branch"
Create two pipelines. Use the lab in this week’s lecture notes as guidance.
The first must use the Jenkinsfile in the master branch.
The second pipeline must use the Jenkins file in the "testing" branch.
For each pipeline, submit your Jenkinsfile and screenshots showing the output from the Console
logs when the builds are complete. Show output to the command: git remote show
origin
Discuss any problems you ran into and how you solved them. Jenkins must run in kubernetes,
as described in the lab.
2
Delete your kubernetes pod:
kubectl delete pod <your jenkins pod name> -n jenkins
Then observe what happens:
kubectl get pods -n jenkins
Turn output to the experiments.
a) Is the pod restarted? Why?
b) What happens to the pipelines you created earlier in jenkins?
c) In the service yaml file, there is a section on "volumes". What is /var/jenkins_home
mapped to? How is this related to question b above?
