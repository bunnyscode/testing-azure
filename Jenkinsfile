pipeline {
   agent any
   stages {
      stage('setup') {
         steps {
            browserstack(credentialsId: '19a621eb-cbe1-4c11-adec-dd57e7029ebe') {
               sh'''
                  export PATH="/opt/homebrew/opt/node@20/bin:$PATH"
                  npm -v
                  node -v
                  npm i
                  npm run sample-test
                  '''
            }
            browserStackReportPublisher 'automate'
         }
      }
    }
  }
