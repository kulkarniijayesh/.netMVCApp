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
                     bat 'cd'
                     bat 'nuget restore'
                     bat 'msbuild'
            }
        }
    }
}
