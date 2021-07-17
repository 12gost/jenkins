pipeline {
    agent any

    stages {
        stage('git clone') {
            steps {
                git branch: 'main', url: 'https://github.com/12gost/ks.git'
            }
        }
		stage('mvn clean') {
            steps {
             sh 'mvn clean'   
            }
        }
		stage('mvn install') {
            steps {
             sh 'mvn install'  
            }
        }
		stage('mvn package') {
            steps {
          sh 'mvn package'
            }
        }
		stage('mvn clean') {
            steps {
          sh 'mvn deploy'
            }
        }
		
    }
}

