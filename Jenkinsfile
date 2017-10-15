pipeline {
  agent {
    docker {
      image 'golang'
      label 'golang'
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
