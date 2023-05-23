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
                PID=`ps -eaf | grep integration-jenkins | grep -v grep | awk '{print $2}'`
				if [[ "" !=  "$PID" ]]; then
				  echo "killing $PID"
				  kill -9 $PID
				fi
                cd target/
                cp *.jar /home/linggar/projects/app-integration-jenkins/
                nohup java -jar integration-jenkins-*.jar > log.log 2>&1 &
                '''
                echo "Finish Deploy"
            }
        }
    }
}