pipeline {
  agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'Local_Maven') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'Local_Maven') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'Local_Maven') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
