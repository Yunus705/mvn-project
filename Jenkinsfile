

pipeline {
  agent any
  tools {
        maven 'Maven'
    }
  stages {
    stage('test') {
      steps {
        sh 'mvn test'
      }
    }
    stage('build') {
      steps {
        sh 'mvn package'
      }
    }
    stage('deoloy on test') {
       steps{
        deploy adapters: [
            tomcat9(
                credentialsId: 'servercredentials', 
                path: '', 
                url: 'http://3.110.218.245:8080'
            )
        ], contextPath: '/app', 
        war: '**/*.war'
       }
    }
    stage('deploy on prod') {
      steps {
        input message: 'continue ?', ok: 'yes'
        deploy adapters: [
            tomcat9(
                credentialsId: 'servercredentials', 
                path: '', 
                url: 'http://13.233.102.131:8080'
            )
        ], contextPath: '/app', 
        war: '**/*.war'
      }
    }
  }
}
