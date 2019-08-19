pipeline {
    agent {label 'jenkins-slave1'}
    stages {
        stage('Build') {
            input {
                message "Should we continue?"
                ok "Yes, we should."
                submitter "alice,bob"
                parameters {
                    string(name: 'PERSON', defaultValue: 'Kalyan Misra', description: 'Approved by $defaultValue')
                }
            } 
            steps {
                echo 'Build Successful'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying'
            }
        }
	stage('Prod') {
	    steps {
		echo 'Deploying to production'
	    }
	}
	
    }
}
