pipeline {
  agent any
  stages {
    stage('fetch code') {
      steps {
        git(url: 'https://github.com/Amruthsraj/html-repo.git', branch: 'main', poll: true)
      }
    }

    stage('install apache') {
      steps {
        sh 'sudo apt install apache2 -y'
      }
    }

    stage('Deploy app') {
      steps {
        sh 'sudo cp -R * /var/www/html/'
      }
    }

  }
}