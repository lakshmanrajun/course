node {
def gitcheckout
stage("checkout")
{
git 'https://github.com/kishoregardas/course.git'
}
mvnhome = tool 'MAVEN_HOME'
stage ("compilation")
{
sh "'${mvnhome}/bin/mvn' compile"
}
stage ("packaging")
{
sh "'${mvnhome}/bin/mvn' package"
}
stage ("result")
{
echo "successfull"
}
}
