pipeline {
    agent {lable "ansible"}

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', credentialsId: 'jenkins-git', url: 'https://github.com/koekkaiwan-git/ansible.git'
            }
        }
        stage('Run Ansible') {
            steps {
                sh 'ansible-playbook -i ansible/inventory.ini ansible/playbook.yml'
            }
        }
    }
}
