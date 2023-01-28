node {
def app
stage ('Clone repositroy'){
checkout scm

}
stage('Build image'){
app= docker.build('alaa/test')}

stage('Test image'){
app.inside{
sh 'echo "passed"'
}
}
stage('Push image')
{
docker.withRegistry('https://hub.docker.com/repositories/alaahamdan','docker.hub.credential')
}
}