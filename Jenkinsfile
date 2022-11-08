pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/giovanniarandaa/curriculum-app', branch: 'dev')
      }
    }

    stage('Shell Script') {
      parallel {
        stage('Shell Script') {
          steps {
            sh 'ls -la'
          }
        }

        stage('Front Test') {
          steps {
            sh 'cd curriculum-front && npm i && npm run test:unit'
          }
        }

      }
    }

  }
}