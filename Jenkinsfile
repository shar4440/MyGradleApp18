pipeline{
  agent any

  tools{
    gradle 'Gradle'
    jdk  'JDK'
  }

  stages{
    stage('checkout'){
      steps{
        git branch: 'master',url: 'https://github.com/shar4440/MyGradleApp18.git'
      }
    }
    stage('Build'){
      steps{
        sh 'gradle build'
      }
    }
    stage(test){

      steps{
        sh 'gradle test'
      }
    }

    stage(run){
      steps{
        sh 'gradle run'
      }
    }
  }

  post{
    success{
      echo "succeed"
    }
    failure{
      echo 'failed'
    }
  }
}
