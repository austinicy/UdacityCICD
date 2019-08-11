pipeline {
    agent any
    stages {
        stage('Upload to AWS') {
            steps {
		        withAWS(region:'us-east-2',credentials:'aws-static'){
	    		    s3Upload(bucket:"udacity-cicd", pathStyleAccessEnabled:true, payloadSigningEnabled: true, file:'index.html' )
		        }
            }
        }
    }
}