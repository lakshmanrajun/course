node {
    def gitcheckout
    stage ("checkout")
{
    git 'https://github.com/kishoregardas/course.git'
}
    mvnhome= tool 'MAVEN_HOME'
    stage ("compilation")
 {
     sh "'${mvnhome}/bin/mvn' compile"
 }   
stage ("packging")
{
    sh "'${mvnhome}/bin/mvn' package"
}
sshagent(['tomcat-dev']) {
    sh 'scp -o StrictHostKeyChecking=no target/*.war ec2-user@172.31.40.65:/opt/apache-tomcat-7.0.93/webapps/'
}
 }
