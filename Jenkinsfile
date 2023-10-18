pipeline {
	agent any
    tools{
        maven 'maven3'
    }
    stages{   
        stage('Build') {
            steps {
                sh 'mvn clean package' // Assuming you are using Maven for building the microservices
            }
        }
		
          stage('Deploy on Application Machine') {
	      steps {
		  sh "nohup java -jar /var/lib/jenkins/workspace/testDjango/target/spring-boot-2-hello-world-1.0.2-SNAPSHOT.jar &"
		}
	}		
    }
}
