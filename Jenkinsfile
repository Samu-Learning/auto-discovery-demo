pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
           echo "build success" 
      }
    }

    stage('Test') {
      steps {
          echo "mvn test starts"
      }
    }

    stage('Deploy Development') {
      steps {
            bat "mvn clean package deploy -DskipMunitTests -DmuleDeploy -DmuleVersion=4.4.0 -Dusername="SPSAMUDHATA" -Dpassword="BookMyShow@1" -DapplicationName=auto-discovery-demo -Denvironment=Sandbox -DbusinessGroup="Training" -DworkerType=MICRO  -Danypoint.platform.client_id=c3fc0bab04e9498ebddf10587743a619 -Danypoint.platform.client_secret=21023af5DcBD417685CD57da7f02313f -Druntime.property=mulesoft -Denv=qa"
            echo "deploy success"      
	  }
	}
  }
}