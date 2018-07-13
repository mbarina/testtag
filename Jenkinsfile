pipeline {
    agent any
    stages {
        stage("test") {
            steps {
                bash '''#!/bin/bash
                  BRANCHS = git ls-remote --heads https://github.com/mbarina/testtag.git | awk '{print $2}'
                  echo $BRANCHS
                '''
            }
        }
    }
}
