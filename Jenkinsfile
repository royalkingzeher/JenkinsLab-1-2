pipeline {
    agent any
    tools {
        maven 'MAVEN_HOME'
    }
      stages {
        stage('Compile') {
            steps {
                sh 'mvn compile'
            }
        }
        stage('Code Analysis') {
            steps {
                // Perform static code analysis (e.g., SonarQube)
            }
        }
        stage('Review') {
            steps {
                // Manual review process
            }
        }
        stage('Unit Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }
        stage('Deploy') {
            steps {
                // Deploy the WAR file to Tomcat
                sh 'cp target/*.war $TOMCAT_HOME/webapps/'
            }
        }
    }
}
