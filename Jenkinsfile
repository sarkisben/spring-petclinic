pipeline {
  agent {label 'Built-In Node'}
  
  stages {
    stage('Hello') {
		steps {
			sh '''
			ansible --version
			ansible-playbook --version
			ansible-galaxy --version
			'''
			}
		}
	}
}