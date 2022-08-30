pipeline {
	agent any
		stages{
			stage(' Anthony N- BranchCreating'){
				steps{
					checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'tonjei1', url: 'https://github.com/tonjei1/sysan11.git']]])
				}
			}
			stage('AnthonyN SystemCheck'){
				steps{
					sh 'bash -x systemCheck.sh'
				}
			}
			stage('test file'){
				steps{
					sh 'bash -x test.sh'
				}
			}
			
		}
}

