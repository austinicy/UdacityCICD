pipeline {
    agent any
    stages {
        stage('Upload to AWS') {
            steps {
		        withAWS(region:'us-east-2',credential:'aws-static'){
	    		    s3Upload(bucket:"audacity-cicd", pathStyleAccessEnabled:true, payloadSigningEnabled: true, file:’index.html’ )
		        }
            }
        }
    }
}