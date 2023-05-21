pipeline {
    agent {
    	node {
    		label "linux && java11"
    	}
    }
    stages {
        stage('Build'){
            steps {
                echo "Start Build"
                sh ("./mvnw clean compile")
                echo "Finish Build"
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