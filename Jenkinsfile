pipeline {
          agent{
            label:"docker"
          }
          stages {
              stage('Build') {
                  steps {
                      echo 'Building..'
                  }
              }
              stage('Test') {
                  steps {
                      echo 'Testing..'
                  }
              }
              stage('Deploy') {
                  steps {
                      echo 'Deploying....'
                      mail body: 'project build successful',
                      from: 'xxxx@yyyyy.com',
                      replyTo: 'xxxx@yyyy.com',
                      subject: 'project build successful',
                      to: 'yyyyy@yyyy.com'
                  }
              }
        }

}
