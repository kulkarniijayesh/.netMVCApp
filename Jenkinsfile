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
    post {
        success {
            echo 'Build Successful! Moving artifacts to S3 bucket...'
            bat 'cd..'
            powershell 'Compress-Archive ".\.NetProjectCI\" build_artifacts.zip'
            bat 'aws s3 cp build_artifacts.zip s3://jenkins-artifacts-essentials-proj/'
        }
        failure {
            echo 'Build Failed!!! Aborting further pipeline.'
        }
    }
}
