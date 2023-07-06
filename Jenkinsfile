pipeline {
	agent any
    stages {
        stage('Build on k8 ') {
            steps {           
                        sh 'pwd'
                        sh 'cp -R helm/* .'
		        sh 'ls -ltr'
                        sh 'pwd'
                        sh '/usr/local/bin/helm upgrade --install ey-app petclinic --set image.repository=https://hub.docker.com/repository/docker/rajat6969/eycloud ----set image.tag=5'
            }           
        }
    }
}
