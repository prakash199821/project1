pipeline {
    agent {
        docker {
			label 'windows'
			image 'maven:3.6.3-alpine' 
            args '-v /root/.m2:/root/.m2' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn clean install -Dlicense.skip=true'
            }
        }
    }
}