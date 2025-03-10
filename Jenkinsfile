pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git credentialsId: 'jenkins-git', url: 'https://github.com/koekkaiwan-git/ansible.git'
            }
        }
        stage('Run Ansible') {
            steps {
                sh 'ansible-playbook -i ansible/inventory.ini ansible/playbook.yml'
            }
        }
    }
}
