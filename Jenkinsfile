pipeline{
    agent any
    environment{
        JAVA_HOME = "C:/Program Files/Java/jdk-21"
        PATH ="${JAVA_HOME}\\bin${env.PATH}"
    }
    stages{
        stage("cloning"){
            steps{
                git url: "https://github.com/User-coder07/checker.git" , branch: 'main'
                // echo 'repository added'
            }
            
        }
        stage("compile"){
            steps{
                bat 'javac pass_cheker.java'
            }
        }
        stage("run java"){
            steps{
                bat 'java pass_cheker'
            }
        }
    }
}
