pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Assume Maven build for Java application
                sh 'mvn clean package'
            }
        }

        stage('Deploy') {
            steps {
                // Use Ansible playbook to deploy
                ansiblePlaybook(
                    playbook: 'ansible/playbook.yml'
                    // inventory: 'ansible/hosts',
                )
            }
        }
    }
}
