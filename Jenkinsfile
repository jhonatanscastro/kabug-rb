pipeline {
   agent {
     docker {
       image 'qaninja/rubywd'
     }
   }

   stages {
      stage('Build') {
         steps {
            echo 'Building or Resolve Dependencies'
            sh 'rm -f Gemfile.lock'
            sh 'bundle install'
         }
        }
        stage('Test') {
         steps {
            echo 'Running regresion Testing'
            sh 'bundle exec cucumber -p ci'
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
