pipeline {
    agent any
      parameters {
          string(name : 'NAME', description : 'Tell me your name')
          text(name : 'EXPE', description : 'Tell about your experience in job')
          choice(name : 'GENDER', choices : ['Male','Female'], description : 'choose gender')
      }
      stages{
          stage('Printing name'){
              steps {
                  script{
                      def name = "${params.NAME}"
                      def gender = "${params.GENDER}"
                      if(gender == "Male"){
                          echo "Mr. $name"
                      } else{
                          echo "Mrs. $name"
                      }
                  }
              }
          }
      
             stage('Printing parameters'){
                      steps{
                          echo "Name :${params.NAME}"
                          echo "Job Experience : ${params.EXPE}"
                      }
                   }
                }
            }
