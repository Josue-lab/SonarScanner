node {
 
 stage('Zero'){
 echo "Hello World"
 }
 stage('SCM') {
 git 'https://github.com/Josue-lab/SonarScanner.git'
 }
 stage('SonarQube analysis') {
 // requires SonarQube Scanner 2.8+
 def scannerHome = tool 'SonarQube Scanner 2.8';
 withSonarQubeEnv('My SonarQube Server') {
 sh "${scannerHome}/bin/sonar-scanner"
 }
 }
}
