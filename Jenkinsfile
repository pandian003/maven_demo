pipeline {
  agent { node { label 'mvn_slave' } }
  stages {
    stage('source') {
      steps {
        git(url: 'https://github.com/hari2912/maven_demo.git', branch: 'master')
      }
    }
    stage('build') {
      steps {
        sh 'mvn clean install'
      }
	}
	stage('Deploy') {
      steps {
        sh 'echo "Build success"
		}
	  }
    }
  }
