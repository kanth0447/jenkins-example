pipeline {
    agent any
  
    stages {
        stage ('Compile Stage') {
            when {
                branch 'master'
            }

            steps {
                sh '''
                      echo "Hello master branch"
                   '''    
            }
        }

        stage ('Testing Stage') {
             when {
                branch 'develop'
            }

            steps {
                sh '''
                      echo "Hello develop branch"
                   '''    
            }
        }


        stage ('Deployment Stage') {
             when {
                branch 'feature-1'
            }

            steps {
                sh '''
                   echo 'Hello feature-1 branch'
                   echo ${JOB_NAME} > job_name.txt
                   export JOB_NAME=$(sed -i 's/\//\_/g' job_name.txt)
                   echo JOB_NAME
                   '''
                                 
            }
        }
    }
}
