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
                sh '''
                cd target/
                cp *.jar /home/linggar/projects/app-integration-jenkins/
                java -jar *.jar
                '''
                echo "Finish Deploy"
            }
        }
    }
}