pipeline {
    agent any

    stages {
        stage("jdvs"){
            steps{
                git branch: 'main', url: 'https://github.com/RaksAniruddha/jenkins-ansible/blob/main/install_apache.yml'
            }
        }
        stage('Hello') {
            steps {
              ansiblePlaybook credentialsId: 'ansible-ssh', disableHostKeyChecking: true, installation: 'ansible2', inventory: '/etc/ansible/hosts', playbook: 'https://github.com/RaksAniruddha/jenkins-ansible/blob/main/install_apache.yml', vaultTmpPath: ''
            }
        }
    }
}
