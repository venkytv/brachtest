pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''#!/bin/bash
BUILD_STATUS=$(( RANDOM % 2 ))
if [[ "$BUILD_STATUS" -eq 0 ]]; then
    echo "$$ Build passed"
    exit 0
fi
echo "$$ Build failed"
exit 1'''
      }
    }
  }
}
