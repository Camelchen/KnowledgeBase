#### Deployment
 * system variables
   ```bat
   ECHO using JAVA 11
   SET JAVA_HOME="C:\Program Files\Java\jdk-11.0.1"
   SET PATH=%PATH%;%JAVA_HOME%\bin
 * user: admin\admin
 
 #### Setup
   * create user token
      > **User > My Account > Security > Generate Tokens**
   
   * Jenkins
```Jenkins
        stage('SonarQube'){
            withEnv(["scannerHome=${tool 'SonarQubeScanner'}"]) {
                withSonarQubeEnv('sonarqube') {
                    bat "${scannerHome}\\bin\\sonar-scanner.bat -Dsonar.projectKey=igrocery-web"
                    //bat "mvn clean package sonar:sonar"
                }
                timeout(time: 10, unit: 'MINUTES') {
                    waitForQualityGate abortPipeline: true
                }
                
            }
        }
````
 #### Configuration
   * exlusive source files
      > **%Project% > Administration > General Settings > Analsysis Scope > Files** <br>
      > DevOps.API/wwwroot/**
