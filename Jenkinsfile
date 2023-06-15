pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
               bat "rmdir  /s /q Selenium-Drag-and-drop-assignment"
                bat "git clone https://github.com/kishancs2020/Selenium-Drag-and-drop-assignment.git"
                bat "mvn clean -f Selenium-Drag-and-drop-assignment"
            }
        }
        stage('install') {
            steps {
                bat "mvn install -f Selenium-Drag-and-drop-assignment"
            }
        }
        stage('test') {
            steps {
                bat "mvn test -f Selenium-Drag-and-drop-assignment"
            }
        }
        stage('package') {
            steps {
                bat "mvn package -f Selenium-Drag-and-drop-assignment"
            }
        }
    }
}
