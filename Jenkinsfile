pipeline {
    agent any

    tools {
        maven 'maven3'
    }

    stages {
        stage('Git Checkout') {
            steps {
                git branch: 'master', url: 'https://github.com/DarshanZ02/Netflix-Pipeline-Project.git'
            }
        }
        stage('Maven Build') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Tomcat Deployment') {
            steps {
                sh 'sudo cp target/NETFLIX-1.2.2.war /home/ubuntu/apache-tomcat-9.0.109/webapps'
            }
        }
    }
}
