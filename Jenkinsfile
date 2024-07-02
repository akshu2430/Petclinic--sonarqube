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
                    playbook: '/var/lib/jenkins/workspace/Jenkins-ansible configuration/ansible/playbook.yml'
                    inventory: '/var/lib/jenkins/workspace/Jenkins-ansible configuration/ansible/inventory',
                )
            }
        }
    }
}
