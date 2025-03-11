pipeline {
    agent {label "ANSIBLE"}

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', credentialsId: 'jenkins-git', url: 'https://github.com/koekkaiwan-git/ansible.git'
            }
        }
        stage('Run Ansible') {
            steps {
                sh '''
                ansible-playbook -i inventory.ini playbook.yml
                '''
            }
        }
    }
}
