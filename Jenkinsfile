pipeline {
    agent any 
    stages {
        stage('Build') {
            steps {
                sh '''
          ansible --version
          ansible-playbook --version
        '''
            }
        }
    }
}
