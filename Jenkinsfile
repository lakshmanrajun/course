node {
def gitcheckout
stage("checkout")
{
git 'https://github.com/kishoregardas/course.git'
}
mvnhome = tool 'MAVEN_HOME'
stage ("packaging")
{
sh "'${mvnhome}/bin/mvn' package"
}
sshagent(['tomcat-id']) {
    // some block
    sh 'ssh -o StrictHostKeyChecking=no target/*.war ec2-user@172.31.36.139:/home/ec2-user/apache-tomcat-7.0.93/webapps
}
stage ("result")
{
echo "successfull"
}
}
