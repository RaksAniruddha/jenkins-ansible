
pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
               git branch: 'main', credentialsId: 'ansible-ssh', url: 'https://github.com/RaksAniruddha/jenkins-ansible/'
            }
        }
        stage("khhvds"){
            steps {
               ansiblePlaybook credentialsId: 'ansible-ssh', installation: 'ansible2', inventory: 'inventory.ini', playbook: 'install_apache.yml', vaultTmpPath: ''
            }
        }
    }
}
