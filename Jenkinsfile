node{
def mavenHome = tool name: "maven3.8.5"
//Checkout Stage
stage('CheckoutCode'){

git branch: 'development', credentialsId: 'e1411605-2c4b-4384-bad4-9b0cc171c9e5',url: 
'https://github.com/chaithanyaakula/maven-web-application.git'
}

//Build Stage
stage('Build'){
sh "$mavenHome/bin/mvn clean package"
}

/*
//generate sonarqube report
stage('SonarQubeReport'){
sh "$mavenHome/bin/mvn sonar:sonar"
}

//upload artifact into artifactory repo
stage('UploadArtifactsIntoNexus'){
sh "$mavenHome/bin/mvn deploy"
}

//deploy app into tomcat server
stage('DeployAppIntoTomcat'){
    sshagent(['d05cc936-03b8-4b18-b362-c5f482e27d36']) {
    sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@15.207.86.171:/opt/apache-tomcat-9.0.60/webapps"
}
} 
*/
}//Node Closing
