pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''#!/bin/bash
echo "hello"
exit'''
        sh '''#!/bin/bash
find . -type f -name "*.sh" -exec cat {} \\;'''
      }
    }
    stage('Testing') {
      parallel {
        stage('Testing1') {
          steps {
            sleep 15
          }
        }
        stage('Testing2') {
          steps {
            sh '''#!/bin/bash
echo "Second Stage1"'''
            sleep 5
          }
        }
      }
    }
    stage('Dev') {
      steps {
        echo 'Going to deploy to Dev'
      }
    }
    stage('Staging') {
      steps {
        echo 'Going to deploy to Staging'
      }
    }
    stage('Production') {
      steps {
        echo 'Going to deploy to Production'
      }
    }
  }
}