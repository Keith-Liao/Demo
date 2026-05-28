pipeline{
    agent none
    tools{
        maven 'maven3'
        jdk 'JDK17' 
    }
    stages{
        stage('window'){
            agent {label 'window-agent'}
            steps{
                bat 'echo window'
                git url:"https://github.com/MaryShen2025/Demo.git",branch:"main",credentialsId:"1e78b6ee-2dcd-4228-b2f7-8f1eb5bc267b"
                dir('demo'){
                    bat 'mvn clean package -DskipTests'
                }
            }
        }
         stage('linux'){
            agent {label 'linux-agent'}
            steps{
               git url:"https://github.com/MaryShen2025/Demo.git",branch:"main",credentialsId:"1e78b6ee-2dcd-4228-b2f7-8f1eb5bc267b"
               dir('demo'){
               
                sh 'echo Linux'
                sh 'ls -la'
                // sh  "cd demo && ls -la"
                sh "mvn clean package -DskipTests"
                }
            }
        }
    }
}

