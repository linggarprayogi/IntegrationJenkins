pipeline {
    agent {
    	node {
    		label "linux && java11"
    	}
    }
    stages {
        stage('Build'){
            steps {
                echo "Start build"
                sh "./mvnw clean compile"
                echo "Finish build"
            }
        }
        
        stage('Deploy'){
            steps {
                echo "Start Deploy"
                echo "Finish Deploy"
            }
        }
    }
}