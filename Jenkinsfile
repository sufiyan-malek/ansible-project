pipeline {
  agent any

  stages {

    stage('Checkout') {
      steps {
        checkout scm
      }
    }

    stage('Verify Ansible') {
      steps {
        sh 'ansible --version'
      }
    }


    stage('Deploy') {
      steps {
        sh 'ansible-playbook -i hosts comment_cronentries.yml'
      }
    }

  }
}
