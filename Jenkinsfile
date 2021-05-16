pipeline {
    agent any
    stages {
	stage('Creating inventory') {
		steps {
			writeFile file: 'hosts.ini', text: """${INVENTORY}"""
		}
	}
        stage('check hosts availability') {
            steps {
                echo 'Hello, Maven'
            }
        }
        stage('Example Test') {
            steps {
                echo 'Hello, JDK'
		    sh "ansible-playbook site.yml -i hosts.ini"
            }
        }
    }
}
