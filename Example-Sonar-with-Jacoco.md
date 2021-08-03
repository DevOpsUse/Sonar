
Step-1: Install sonar as per other document - sonar-setup-using-docker.md

Step-2: Create project- Login to sonar >> Click on plus symbol >> create new project

![image](https://user-images.githubusercontent.com/24622526/128054553-43adb0c1-59df-4710-b307-a0a75edbba04.png)

Enter the project name and click setup (this project name we will have to pass an argument to sonar maven command as one of the sonar property "sonar.projectKey"

![image](https://user-images.githubusercontent.com/24622526/128054665-aed2497c-7c54-47d2-9852-b70d9c149982.png)

Give the suitable name for token for authentication and then click generate

![image](https://user-images.githubusercontent.com/24622526/128054784-90f36ecc-6269-420b-bd61-0f212769ae6e.png)

![image](https://user-images.githubusercontent.com/24622526/128054895-84d644c4-2648-4717-a006-26770fd6d89d.png)

Copy the token and note down somewher in notepad

Step-3: clone the code from https://github.com/CalculatorApps/Addition.git and run the below command

> Note: In the below command, you need to update the value of "sonar.projectKey=AdditionProject", "sonar.host.url", and "sonar.login" which we generated while creating project in Sonar.

	mvn clean package org.codehaus.mojo:sonar-maven-plugin:3.7.0.1746:sonar -Pjacoco -DreleaseVersion=1.0 -Dsonar.projectKey=AdditionProject -Dsonar.host.url=http://3.84.135.178:9000 -Dsonar.login=093e48fff29543c0b96d4762878022ed7b8ced69 -Dsonar.coverage.jacoco.xmlReportPaths=target\jacoco-ut\jacoco.xml


![image](https://user-images.githubusercontent.com/24622526/128055600-3d55e2c1-6bfa-4cf1-9181-440b61da7da9.png)




    
