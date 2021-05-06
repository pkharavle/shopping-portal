pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'npm install'
      }
    }

    stage('test') {
      steps {
        sh 'npm test'
      }
    }

    stage('package') {
      steps {
        sh 'npm run package'
      }
    }

    stage('archive') {
      steps {
        archiveArtifacts '**frontend-0.0.2.zip'
      }
    }

  }
  tools {
    nodejs 'nodejs'
  }
  post {
    always {
      echo 'this pipeline is for shopping-portal application...'
    }

  }
}