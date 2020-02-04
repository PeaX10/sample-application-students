# DevOps: TP2 - Github, Travis CI, Sonarcloud
*__Pipeline tools__*  
- Travis CI
- Gitlab CI
- Jenkins
- Bitbucket Pipeline  
- Bitrise
- Circle CI
  
## Setup Travis CI
First link our Github account to Travis CI. Then add our repositories on Travis CI.  
Most of CI services uses a yaml file to describes steps that need to be done (except for Jenkins which uses a Groovy file).  
Let's write our first travis.yaml file:  
``
language: java  
script: mvn clean verify
``
Once everything is setup, we push the code on Github. It triggers the .travis.yml file and execute the ``mvn clean verify``.  

*__What is it supposed to do ?__*  
``mvn clean verify`` run the build life cycle "clean" which is going to clean the "target" directory if exist so we are sure that the ".jar" file is regenerated.  
The ``verify`` will eache lifecycles before (eg: validate, compile etc.) and the Unit tests as well as the integration tests. The results of integration tests are verified to ensure the quality of these results.  
![Travis CI first push](https://raw.githubusercontent.com/PeaX10/sample-application-students/master/img/logsTravisCi.png)
__Unit tests__: it tests each module individually. These tests can be done at anytime so it is easier to see errors.  
__Integration tests__: it is almost the opposite of unit tests. It tests a group of module to see if they interact correctly that is why it is more difficult to see where the error is.  
  
*__What is a "db changelog job" ?__*  
This application create the tables before the API application populate it. It also ensure versions change when creating new tables.  

