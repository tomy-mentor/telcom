


pipeline {
    agent { label 'master' }
    stages {
        stage('first stage:copy files') {
            steps {
                echo "Copy files from github"
                
		sh 'pwd'
		sh 'cd'
		sh 'pwd'	
		sh """
		pwd
 		rm -rf telcom-pipeline-new
		mkdir telcom-pipeline-new
		cd telcom-pipeline-new
		wget https://raw.githubusercontent.com/tomy-mentor/telcom/main/smote_rf_model_2
                wget https://raw.githubusercontent.com/tomy-mentor/telcom/main/smote_rf_model
                wget https://raw.githubusercontent.com/tomy-mentor/telcom/main/model_features.pkl
		wget https://raw.githubusercontent.com/tomy-mentor/telcom/main/df_deploy.pkl
                wget https://raw.githubusercontent.com/tomy-mentor/telcom/main/deployment.ipynb
		wget https://raw.githubusercontent.com/tomy-mentor/telcom/main/churn2.ipynb
		wget https://raw.githubusercontent.com/tomy-mentor/telcom/main/app.py
		wget https://raw.githubusercontent.com/tomy-mentor/telcom/main/WA_Fn-UseC_-Telco-Customer-Churn.csv
		wget https://raw.githubusercontent.com/tomy-mentor/telcom/main/.ipynb_checkpoints/app-checkpoint.py		
		wget https://raw.githubusercontent.com/tomy-mentor/telcom/main/.ipynb_checkpoints/churn2-checkpoint.ipynb
		wget https://raw.githubusercontent.com/tomy-mentor/telcom/main/.ipynb_checkpoints/deployment-checkpoint.ipynb

		ls
		"""
            }



       }
	 stage('build') {
            steps {
		sh """
		pwd
		ls
		cp q310-ubuntu.pem /var/lib/jenkins/workspace/telcom-pipeline/telcom-pipeline-new
		cd /var/lib/jenkins/workspace/telcom-pipeline/telcom-pipeline-new
		ls
		chmod 400 q310-ubuntu.pem
		scp smote_rf_model_2 ec2-3-95-138-59.compute-1.amazonaws.com:/home/ec2-user
		"""

		echo "Testing"
                echo "Tomy is training"
                sh 'echo second step'
                sh 'echo another step'
            
            }

        }
    }
}
