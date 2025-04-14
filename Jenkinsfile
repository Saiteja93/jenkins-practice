pipeline {
    agent {
        label 'agent-1'
    }
    options{
        timeout(time: 10, unit: 'seconds')
         disableConcurrentBuilds()
    }
     stages {
        stage('Build') {
            steps {
                sh 'echo This is Build'
                sh 'sleep 10'
            }
        }
        stage('Test') {
            steps {
                sh 'echo This is test'
              
            }
        }
        stage('Deploy') {
          
            steps {

                    sh 'echo This is deploy'
                    //error 'pipeline failed'

            }
        }
    }
    

    post {
        always {
            echo " this section runs always"
        }
        success {
            echo "this section run when pipeline sucecess"
        }
        failure {
            echo "this section runs when pipeline failed"
        }
    }
}
        
