pipeline {
	agent any
	stages {
		stage('Build') {
			steps {
				echo 'Building'
			      }
		}
		stage('Deploy') {
			steps {
				sh "/usr/local/bin/aws cloudformation create-stack --stack-name myec2stack2 --template-body file://ec2.json --parameters ParameterKey=KeyName,ParameterValue=jenkins_aws ParameterKey=InstanceType,ParameterValue=t2.micro"
			      }
		}
	}
}
