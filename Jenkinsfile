pipeline {

  agent jenkins_agent

  options {

    buildDiscarder logRotator(artifactDaysToKeepStr: '15', artifactNumToKeepStr: '5', daysToKeepStr: '', numToKeepStr: '5')

  }

  stages {

    stage('Hello') {

      steps {

        sh '''

          java -version

        '''

      }

    }

    stage('cat README') {

      when {

        branch "dev"

      }

      steps {

        sh '''

          cat README.md

        '''

      }

    }

  }

}
