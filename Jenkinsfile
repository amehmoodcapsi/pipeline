pipeline {
  agent any
  stages {
    stage('firstStage') {
      steps {
        sh '''#!/bin/bash
echo "hello"
exit'''
      }
    }
    stage('Second Stage') {
      parallel {
        stage('Second Stage') {
          steps {
            sleep 15
          }
        }
        stage('Second Stage1') {
          steps {
            sh '''#!/bin/bash
echo "Second Stage1"'''
            sleep 5
          }
        }
      }
    }
  }
}