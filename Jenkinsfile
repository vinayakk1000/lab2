pipeline{
  agent any
  stages{
    stage( 'Checkout'){
      steps{
            git url :'https://github.com/Sahilsalunkhe001/my_first_rep.git',branch:'master'
      }
    }
    stage('Build Image'){
    steps{
       bat 'docker build -t mywebsite .'
    }
    }
    stage('Stop Old Containers'){
    steps{
      bat 'docker stop mycount || exit 0'
      bat ' docker rm mycount || exit 0'
    }
    }
    stage(' Run Image - containerize'){
      steps{
      bat 'docker run -d -p 7000:80 --name mycount mywebsite'
      }
      }
  }
}
