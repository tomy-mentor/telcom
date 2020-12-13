


pipeline {
    agent { label 'master' }
    stages {
        stage('first stage:copy files') {
            steps {
                echo "Copy files from github"
                sh 'ls'
		sh 'pwd'
		sh 'sudo rm -rf telcom-pipeline'
		sh 'mkdir telcom-pipeline'
		sh 'wget https://raw.githubusercontent.com/tomy-mentor/telcom/main/smote_rf_model_2'
                sh 'wget https://raw.githubusercontent.com/tomy-mentor/telcom/main/smote_rf_model'
                sh 'wget https://raw.githubusercontent.com/tomy-mentor/telcom/main/model_features.pkl'
		sh 'wget https://raw.githubusercontent.com/tomy-mentor/telcom/main/df_deploy.pkl'
                sh 'wget https://raw.githubusercontent.com/tomy-mentor/telcom/main/deployment.ipynb'
		sh 'wget https://raw.githubusercontent.com/tomy-mentor/telcom/main/churn2.ipynb'
		sh 'wget https://raw.githubusercontent.com/tomy-mentor/telcom/main/app.py'
		sh 'wget https://raw.githubusercontent.com/tomy-mentor/telcom/main/WA_Fn-UseC_-Telco-Customer-Churn.csv'
		sh 'wget https://raw.githubusercontent.com/tomy-mentor/telcom/main/.ipynb_checkpoints/app-checkpoint.py'		
		sh 'wget https://raw.githubusercontent.com/tomy-mentor/telcom/main/.ipynb_checkpoints/churn2-checkpoint.ipynb'
		sh 'wget https://raw.githubusercontent.com/tomy-mentor/telcom/main/.ipynb_checkpoints/deployment-checkpoint.ipynb'

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
