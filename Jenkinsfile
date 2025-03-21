pipeline {
    agent any
    
    environment {
        JAVA_HOME = "C:/Program Files/Java/jdk-21"
        PATH = "${JAVA_HOME}\\bin;${PATH}"
    }
    
    stages {
        stage('Clone Repository') {
            steps {
                git url: 'https://github.com/User-coder07/checker.git', branch: 'main'
            }
        }
        
        stage('Build') {
            steps {
                script {
                    echo 'Building Java Project...'
                    bat '"%JAVA_HOME%\\bin\\javac" pass_cheker.java'
                }
            }
        }
        
        stage('Run') {
            steps {
                script {
                    echo 'Running Java Application...'
                    bat '"%JAVA_HOME%\\bin\\java" pass_cheker'
                }
            }
        }
    }
}
