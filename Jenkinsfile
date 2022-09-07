pipeline{
    agent any 
    stages{
        stage('clone'){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'jenkinsgit', url: 'https://github.com/YomiPounds/pounds-repo.git']]])
            }
        }
        stage('para-stage'){
            parallel{
                stage('para-stage1'){
                    steps{
                        echo "this is a trial"
                    }
                }
                stage('para-stage2'){
                    steps{
                        sh 'whoami'
                    }
                }
            }
        }
    }
}