pipeline {
    agent any

    tools {
        // Use specfically installed jdk and maven
        jdk "java-17"
        maven "maven-3.9.1"
    }

    stages {
        stage('Build') {
            steps {
                // Get some code from a GitHub repository
                git 'https://github.com/julius-hs/hapi-fhir-jpaserver.git'

                // Run Maven on a Unix agent.
                // sh "mvn -Dmaven.test.failure.ignore=true clean package"
                sh "mvn clean install"
                sh "ls"
            }
        }
    }
}

