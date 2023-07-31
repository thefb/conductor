pipeline {
  agent {
    dockerfile {
      filename 'docker/server/Dockerfile'
    }

  }
  stages {
    stage('clone') {
      steps {
        sh 'git clone https://github.com/thefb/conductor.git'
      }
    }

    stage('docker') {
      steps {
        sh '''cd conductor

docker compose -f "docker/docker-compose.yaml" up -d --build'''
      }
    }

  }
}