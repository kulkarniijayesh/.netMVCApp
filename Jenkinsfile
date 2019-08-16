pipeline {
    agent {label 'windows'}
    
    stages {
        stage('INIT') {
            steps {
                echo 'Initiating CI for .Net project...'
            }
        }
        
        stage('Build') {
            steps {
                 echo 'Building..'
                 bat 'dir'
            }
        }
    }
}
