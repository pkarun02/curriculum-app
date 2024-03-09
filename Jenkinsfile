pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/pkarun02/curriculum-app', branch: 'dev')
      }
    }

    stage('Log') {
      parallel {
        stage('Log') {
          steps {
            sh 'ls -la'
          }
        }

        stage('Build /Shell script') {
          steps {
            sh 'docker build -f curriculum-front/Dockerfile .'
          }
        }

      }
    }

  }
}