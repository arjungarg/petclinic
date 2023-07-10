pipeline {
	agent any
    stages {
        stage('Build on k8 ') {
            steps {           
                        sh 'pwd'
                        sh 'cp -R helm/* .'
		        sh 'ls -ltr'
                        sh 'pwd'
		        sh 'cd petclinic'
		        sh '--set image.repository = $BUILD_NUMBER'
                        sh 'ansible-playbook deploy.yml'

            }           
        }
    }
}
