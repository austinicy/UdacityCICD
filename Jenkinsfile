pipeline {
    agent any
    options {
	withAWS(credential:'aws-static'){
		s3Upload(bucket:"audacity-cicd", path:'/', workingDir:'dist')
	}
    }
    stages {
        stage('Upload to AWS') {
            steps {
                sh 'echo "Hello World"'
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
            }
        }
    }
}