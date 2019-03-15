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
}
stage ("result")
{
echo "successfull"
}
}
