pipeline {
    agent {
        docker {
            image 'maven:3-alpine' 
            args '-v /data/mvn:/root/.m2' 
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
