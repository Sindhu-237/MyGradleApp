pipeline{
	agent any
	
	tools{
		gradle 'Gradle'
		jdk 'JDK11'
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
		stage('Test'){
			steps{
				sh'gradle test'
			}
		}
		stage('Run Application'){
			steps{
				sh'gradle run'
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
		
