pipeline {
   agent any

   stages {
      stage('Build') {
         steps {
            echo 'Building or Resolve Dependencies'
            sh 'bundle install'
         }
        }
        stage('Test') {
         steps {
            echo 'Running regresion Testing'
         }
        }
        stage('UAT') {
         steps {
            echo 'Waiting For User Acceptance'
            input(message: 'Go to Production?', ok: 'Yes')
         }
        }
        
        stage('prod') {
            steps {
                echo 'Webapp is Ready :D'
         }
        }
   }
}
