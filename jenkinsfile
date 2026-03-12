pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/MCA25104/Test.git'
            }
        }

      stage('Publish'){
        steps{
          publishHTML([
            allowMissing:true,
            alwaysLinkToLastBuild:false,
            keepAll:false,
            reportDir:'.',
            reportFiles:'test.html',
            reportName:'My HTML Pipe Publish'
           ])
        }
     }
    }
}
