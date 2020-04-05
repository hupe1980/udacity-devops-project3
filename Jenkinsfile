pipeline {
    agent any
    stages {
        stage('Upload to AWS') {
            steps {
                withAWS(region:'eu-central-1',credentials:'aws-udacity-devops-project3') {
                    s3Upload(pathStyleAccessEnabled:true, payloadSigningEnabled: true, file:'index.html', bucket:'udacity-devops-project3-jenkins')
			    }	
		    }
        }
    }
}
