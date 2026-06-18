pipeline{
agent any{
	tools{
		maven 'Maven'
		}
	stages{
		stage('Checkout'){
			steps{
				git branch:'main',url: 'https://github.com/vinaykumargunjalli18/MYMAVENAP'
				}
			}
		stage('Build'){
			steps{
				sh 'mvn clean package'
				}
			}
		stage('test'){
			steps{
				sh 'mvn test'
				}
			}
		stage('Run Application'){
			steps{
				sh 'java -jar target/MyMavenApp-1.0-SNAPSHOT.jar'
				}
			}
		}
		post{
			sucess{
				echo 'Build and deoployment sucessful'
				}
			failure{
				echo 'Build failure'
				}
			}
		}
}
