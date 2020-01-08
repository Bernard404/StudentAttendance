pipeline {
    agent any
    stages {
        stage('Fetch') {
            steps {
                sh 'git clone "https://github.com/Bernard404/studentAttendance.git"'
            }
        }
        
        stage('Test') {
            steps {
                sh 'mvn test -f "studentAttendance"'
            }
        }
        stage('Cleanup') {
            steps {
                deleteDir()
            }
        }
    }
}
