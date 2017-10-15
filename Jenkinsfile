pipeline {
  agent {
    docker {
      image 'golang:1.9'
      label 'golang-1.9'
    }
  }

  stages {
    stage('build') {
      steps {
        checkout([$class: 'GitSCM', branches: [[name: '*/master']],
          userRemoteConfigs: [[url: 'https://github.com/timcurless/chapter10-services-search.git']]])
        
      }
    }
  }
}
