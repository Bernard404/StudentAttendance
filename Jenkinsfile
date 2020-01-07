pipeline {
    agent any
    stages {
        stage('Fetch') {
            steps {
                sh 'git clone "https://github.com/Bernard404/StudentAttendance.git"'
            }
        }
        stage('Build') {
            steps {
                 sh 'mvn clean -f "StudentAttendance"'
                 sh 'mvn compile -f "StudentAttendance"'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test -f "StudentAttendance"'
            }
        }
        stage('Cleanup') {
            steps {
                deleteDir()
            }
        }
    }
}
