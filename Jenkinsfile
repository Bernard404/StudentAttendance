pipeline {
    agent any
    stages {
        stage('Clean') {
            steps {
                deleteDir()
            }
        }
        stage('Pull') {
            steps {
                sh 'git clone "https://github.com/Bernard404/studentAttendance.git"'
            }
        }
        stage('Testing') {
            steps {
                sh 'mvn test -f "studentAttendance"'
            }
        }
        stage('Build') {
            steps {
                 sh 'mvn clean -f "studentAttendance"'
                 sh 'mvn compile -f "studentAttendance"'
            }
        }
        
    }
}
