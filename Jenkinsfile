pipeline {
	agent any
    stages {
        stage('Build on k8 ') {
            steps {           
                        sh 'pwd'
                        sh 'cp -R helm/* .'
		        sh 'ls -ltr'
                        sh 'pwd'
		        sh 'yq -i '.image.repository = $BUILD_NUMBER' values.yaml'
                        sh 'ansible-playbook deploy.yml'

            }           
        }
    }
}
