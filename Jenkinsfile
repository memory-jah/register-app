pipeline {
    agent { labale 'Jenkins-Agent' }
    tools {
          jdk 'Java17'
          maven  'Maven3'
    }
    satges{
          stage( "cleanup Workspace"){
                  steps {
                  cleanWs()
                  }
          }

          stage ("Checkout from SCM"){
                  steps {
                      git branch: 'main', credentialsId: 'github', url: 'https://github.com/Ashfaque-9x/register-app'
                  }
           }

          stage ("Build Application"){
                  Steps {
                  sh "mvn clean package"
                  }
          }

          stage ("Test Application"){
                  steps { sh "mvn test"
                  }
          }   
    }
}

     
       
