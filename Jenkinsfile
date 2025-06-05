pipeline{
	agent any
	tools{
		maven 'Maven'
	}
	stages{
		stage('Checkout'){
			steps{
				git branch:'master', url:"https://github.com/MedhiniKaraba/MavenDemo.git"
			}
		}
		stage('Build'){
			steps{
				sh 'mvn clean install'
			}
		}
		stage('Test'){
			steps{
				sh 'mvn test'
			}
		}
		stage('Run Application'){
			steps{
				sh 'java -jar MavenDemo-1.0-SNAPSHOT.jar'
			}
		}
	}
	post{
		success{
			echo 'Build successful'
		}
		failure{
			echo 'Build failure'
		}
	}
}

