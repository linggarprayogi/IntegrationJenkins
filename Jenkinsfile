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
                sh 'mvn clean'
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