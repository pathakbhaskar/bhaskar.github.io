pipeline {
  agent any
  stages {
    stage('Fetch Code') {
      steps {
        git(url: 'https://github.com/pathakbhaskar/web.git', branch: 'master', poll: true)
      }
    }

    stage('Install Apache') {
      steps {
        sh 'sudo apt install apache2 -y'
      }
    }

    stage('Deploy Code') {
      steps {
        sh 'sudo cp -R * /var/www/html/'
      }
    }

  }
}