number= sh 'cat /var/lib/jenkins/jobs/EYpipeline/nextBuildNumber'
pipeline {
	agent any
    stages {
        stage('Build on k8 ') {
            steps {           
                        sh 'pwd'
                        sh 'cp -R helm/* .'
		        sh 'ls -ltr'
                        sh 'pwd'
		        sh 'cat /var/lib/jenkins/jobs/EYpipeline/nextBuildNumber'
                        sh '/usr/local/bin/helm upgrade --install ey-app petclinic --set image.repository=rajat6969/eycloud  --set image.tag=number'

            }           
        }
    }
}
