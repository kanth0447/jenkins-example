def allJob = env.JOB_NAME.tokenize('/') as String[];
def projectName = allJob[0];
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
                sh "echo 'Hello feature-1 branch'"
                sh "echo ${projectName}"
                sh "echo ${projectName}_${GIT_BRANCH}"
                sh 'echo ${projectName}_${GIT_BRANCH}'
                sh '''
                    echo ${projectName}_${GIT_BRANCH}
                   '''
                
            }
        }
    }
}
