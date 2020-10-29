CODE_CHANGES = getGitChanges()
pipeline {
      agent any 
      environment{
      NEW_VERISON = '1.3.0'
      
      }
       stages {
                     
            stage ("build"){
                   when {
                        expression {
                        BRANCH NAME == 'main' && CODE_CHANGES == true
                        }
                  }
            steps {
                  echo 'Building an application....'
                  echo "Building version ${NEW_VERSION)" 
                  }
                          }
            stage ("test"){
                  when {
                        expression {
                        BRANCH NAME == 'main' 
                        }
                  }
            steps {
                echo 'Testing the application'
                  }
                          }
            stage ("deploy"){
            steps {
                echo 'Deploy the application'
                  }
                    }
                     }
      post {
            always {
                        
            }
            failure {
            
            
            }
            
      }
      
         }
