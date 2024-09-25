pipeline {
 agent any 


  stages {
   stage('git checkout'){
    steps{
      git branch: 'main', url: 'https://github.com/Penda1604/aws-cicd2.git'
    }
   }
   stage('test'){
    steps{
        sh 'echo test'
   }
  }
}
}