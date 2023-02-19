pipeline{
  agent any
  stages{
    stage('Build'){
      steps{
        echo 'Building ...'
        sh 'g++ PES1UG20CS368.cpp -o PES1UG20CS368'
        build job: 'PES1UG20CS368-1'
        echo 'Build stage has been completed successfully'
      }
    }
    stage('Test'){
      steps{
        echo 'Testing ...'
        sh './nothing'
        echo 'Test stage has been completed successfully'
      }
    }
   stage('Deploy'){
      steps{
        echo 'Deploying ...'
        sh 'cat PES1UG20CS368.cpp'
        echo 'Deploy stage has been completed successfully'
      }
    }
  }
  post{
    failure{
      echo 'Pipeline Failed'
    }
  }
}
