pipeline {
    agent any

    stages {
        stage("jdvs"){
            steps{
              git branch: 'main', credentialsId: 'ansible-ssh', url: 'https://github.com/RaksAniruddha/jenkins-ansible/'
            }
        }
        stage('Hello') {
            steps {
              ansiblePlaybook credentialsId: 'ansible-ssh', installation: 'ansible2', inventory: 'inventory.ini', playbook: 'install_apache.yml', vaultTmpPath: ''
        }
    }
}
