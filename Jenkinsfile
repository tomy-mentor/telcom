


pipeline {
    agent { label 'master' }
    stages {
        stage('first stage:copy files') {
            steps {
                echo "Copy files from github"
                sh 'wget https://raw.githubusercontent.com/tomy-mentor/telcom/main/smote_rf_model_2'
                sh 'ls'
            }
       }
	 stage('build') {
            steps {
                echo "Clarusway_Way to Reinvent Yourself"
                sh 'echo second step'
                sh 'echo another step'
            
            }

        }
    }
}
