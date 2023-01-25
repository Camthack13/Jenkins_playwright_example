
pipeline {
  agent { 
  label 'agent-1'
  }
  stages {
    stage('test') {
      steps {
        sh '''
          npx playwright test --list
          npx playwright test
        '''
      }
    }
    stage('email') {
      steps {
        mail (to: 'camronthackeray@homecarepulse.com',
                        subject: "Job  failed",
                        body: "Please visit  for further information"
                );
      }
    }
  }
}