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
                branch 'feature/cicd-pcf'
            }

            steps {
                sh '''
                      echo "Hello feature/cicd-pcf branch"
                   '''    
            }
        }
    }
}
