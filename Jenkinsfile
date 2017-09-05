pipeline {
        agent {
          label 'docker'
        }
        currentBuild.result = "SUCCESS"
        try{
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
        }catch(err){
            currentBuild.result = "FAILURE"

            mail body: "project build error is here: ${env.BUILD_URL}" ,
            from: 'xxxx@yyyy.com',
            replyTo: 'yyyy@yyyy.com',
            subject: 'project build failed',
            to: 'zzzz@yyyyy.com'
            throw err
        }

}
