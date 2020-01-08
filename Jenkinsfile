pipeline {
    agent any
    stages {
        stage('Fetch') {
            steps {
                sh 'git clone "https://github.com/Bernard404/studentAttendance.git"'
            }
        }
        stage('Cleanup') {
            steps {
                deleteDir()
            }
        }
        
        stage('Test') {
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
