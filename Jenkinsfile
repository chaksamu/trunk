pipeline{
    agent any 
    
    stages{
        stage('SCM Checkout') {
            steps{
                git branch: 'master', url: 'https://github.com/chaksamu/trunk.git'
            }
        }
        stage('Execute Ansible'){
            steps{
                //ansiblePlaybook credentialsId: 'allinone', disableHostKeyChecking: true, installation: 'ansible2', inventory: 'hosts', playbook: 'copy.yml'
                //ansiblePlaybook credentialsId: 'allinone', disableHostKeyChecking: true, installation: 'ansible2', inventory: 'hosts', playbook: 'uploadanduntar.yml'
                //ansiblePlaybook credentialsId: 'allinone', disableHostKeyChecking: true, installation: 'ansible2', inventory: 'hosts', playbook: 'untar.yml'
                //ansiblePlaybook credentialsId: 'allinone', disableHostKeyChecking: true, installation: 'ansible2', inventory: 'hosts', playbook: 'project_name.yml'
		ansiblePlaybook colorized: true, credentialsId: 'allinone', disableHostKeyChecking: true, installation: 'ansible2', inventory: 'hosts.d/sredev/sredev.ini', playbook: 'project_name.yml'
            }
        }
    }
}
