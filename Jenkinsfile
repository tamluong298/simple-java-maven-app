pipeline {
    agent {
        docker {
            //image 'maven:3-alpine'
            image 'qasymphony/build:gradle-4.2-aws-cli-v2'
            args '-v /root/.m2:/root/.m2' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
