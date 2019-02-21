pipeline {
    agent any
//    tools {
//        maven 'Maven3.6.0'
//        jdk 'JDK1.8'
//    }
    stages {
        stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                npm install
		   '''
            }
        }

        stage ('Build') {
            steps {
                //sh 'mvn -Dmaven.test.failure.ignore=true install'
                sh "build...."
            }
            post {
                success {
                echo "success..."    
		//junit 'target/surefire-reports/**/*.xml'
                }
            }
        }
    }
}