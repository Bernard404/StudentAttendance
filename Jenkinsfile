pipeline {
    agent any
    stages {
        stage('Fetch') {
            steps {
                sh 'git clone "https://github.com/m-codes/student-attendance-jenkins.git"'
            }
        }
        stage('Build') {
            steps {
                 sh 'mvn clean -f "student-attendance-jenkins"'
                 sh 'mvn compile -f "student-attendance-jenkins"'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test -f "student-attendance-jenkins"'
            }
        }
        stage('Cleanup') {
            steps {
                deleteDir()
            }
        }
    }
}
