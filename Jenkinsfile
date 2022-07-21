pipeline {
  agent any
  stages {
    stage('Setup') {
      parallel {
        stage('Setup') {
          steps {
            sh '''#!/bin/bash

export VERSION="0.0.0CI"
echo ---------------------------------------------------------------------------
echo Build Information
echo ---------------------------------------------------------------------------
echo "Working on : $JOB_NAME"
echo "Workspace  : $WORKSPACE" 
echo "Revision   : $SVN_REVISION"
echo "Build      : $BUILD_NUMBER"
echo "Deploy to  : $DEPLOY_TO"
echo ---------------------------------------------------------------------------
echo "GIT_COMMIT : $GIT_COMMIT" 
echo "GIT_BRANCH : $GIT_BRANCH"
echo ---------------------------------------------------------------------------
'''

 stage('Get Version Number') {
          steps {
            echo 'Get Version Number'
            load 'versionInput.groovy'
          }
        }

}
}
}
}
}
}
