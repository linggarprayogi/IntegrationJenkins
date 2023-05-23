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
                sh 'mvn clean install package'
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