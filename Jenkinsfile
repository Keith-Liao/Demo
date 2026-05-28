pipeline{
    agent any
    tools{
        maven 'maven'
        jdk 'JDK17' 
    }
    stages{
        // stage('window'){
        //     agent {label 'window-agent'}
        //     steps{
        //         bat 'echo window'
        //         git url:'https://github.com/Keith-Liao/Demo.git',branch:'main',credentialsId:'e2432a4a-dc19-4275-bacd-50c961bc00d4'
        //         dir('demo'){
        //             bat 'mvn clean package -DskipTests'
        //         }
        //     }
        // }
         stage('linux'){
            // agent {label 'Built-In Node'}
            steps{
               git url:'https://github.com/Keith-Liao/Demo.git',branch:'main',credentialsId:'e2432a4a-dc19-4275-bacd-50c961bc00d4'
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
