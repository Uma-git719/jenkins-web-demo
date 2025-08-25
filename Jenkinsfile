pipeline {
    agent any

    stages {
        stage('Deploy to Azure VM') {
            steps {
                sshagent(['azure-vm-ssh']) {
                    sh '''
                        scp index.html azureuser@<VM_PUBLIC_IP>:/var/www/html/index.html
                    '''
                }
            }
        }
    }
}
