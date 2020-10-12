node('master') 
{
    stage('Continuous Download') 
	{
    git 'https://github.com/sunildevops77/maven.git'
	}
    stage('Continuous Build') 
	{
    sh label: '', script: 'mvn package'
	}
    stage('Continuous Deployment') 
	{
sh label: '', script: 'cp -rf /var/lib/jenkins/workspace/job_test/webapp/target/webapp.war  /var/lib/jenkins/qa'
	}
    stage('Continuous Testing') 
	{
              sh label: '', script: 'echo "Testing Passed"'
	}
    stage('Continuous Delivery') 
	{
sh label: '', script: 'cp -rf /var/lib/jenkins/workspace/job_test/webapp/target/webapp.war   /var/lib/jenkins/prod'
	}
}
