pipeline{
    agent any
    stages{
        stage('SCM checkout'){
            steps{
                git 'https://github.com/PUSH-PRAG/myapp-ansible'
                }
            }
        stage('execute ansible'){
            steps{
                ansiblePlaybook credentialsId: 'privatekey', disableHostKeyChecking: true, installation: 'ansible', inventory: 'dev.inv', playbook: 'apache.yml'
                }
            }
        }
    }
