pipeline {
    agent any

    stages {
        stage("jdvs"){
            steps{
             git branch: 'main', url: 'https://github.com/RaksAniruddha/jenkins-ansible'
            }
        }
        stage('Hello') {
            steps {
                ansiblePlaybook credentialsId: 'ansible-ssh', installation: 'ansible2', inventory: 'https://github.com/RaksAniruddha/jenkins-ansible/blob/main/inventory.ini', playbook: 'https://github.com/RaksAniruddha/jenkins-ansible/blob/main/install_apache.yml', vaultTmpPath: ''
            }
        }
    }
}
