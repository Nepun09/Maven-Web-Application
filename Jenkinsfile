pipeline{
    agent any
    stages{
        stage('cloning the code from REPO'){
            steps{
                echo "cloning the code -MaveWeb APP"
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Nepun09/Maven-Web-Application.git']]])
            }
        }
        stage('building the Cloned code'){
            steps{
            echo "building the Cloned code"
            sh "mvn clean install"
            }
        }
	    stage('TESTING THE CODE') {
            steps {
                echo "Testing the code by running Unit Test Cases"
            }
        }
        
        stage('DEPLOYING THE APPLICATION ON SERVERS') {
            steps {
                echo "Deployment in Test Levels"
            }
        }
        
        stage('RELEASE ON TO PRODUCTION SERVERS') {
            steps {
                echo "Deployment on PROD SERVERS"
            }
        }
        
        stage('POST-BUILD NOTIFICATION TO DEV TEAM') {
            steps {
                echo "Trigger mail to devteam@gmail.com"
            }
        }
    }
}
