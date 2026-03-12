

  pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/vinayakk1000/lab2.git'
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
