pipeline{
	agent any
	
	tools{
		gradle 'Gradle'

	}
	stages{
		stage('Checkout'){
			steps{
				git branch:'master',url:'https://github.com/Sindhu-237/MyGradleApp.git'
			}
		}
		stage('Build'){
			steps{
				sh'gradle build'
			}
		}
	
		stage('Run'){
			steps{
				sh'gradle run'
			}
		}
		
		stage('Custom Task'){
			steps{
				sh'gradle display'
			}
		}
	}
	post{
		success{
			echo'Build success'
		}
		failure{
			echo'Build failure'
		}
	}
}
		
