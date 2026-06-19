pipeline{
	agent any
	stages{
		stage('Checkout'){
			steps{
				git 'https://github.com/bitcsedevops214/CS255.git'
			}
		}
		stage('Compile'){
			steps{
				sh 'mvn compile'
			}
		}
		stage('Test'){
			steps{
				sh 'mvn test'
			}
		}
		stage('Package'){
			steps{
				sh 'mvn package'
			}
		}
	}
	post{
		success{
			echo 'Build Succesful'
		}
		failure{
			echo 'Build Failure'
		}
	}
}
