pipeline

{
agent any
stages

{

 stage ('Build')

 {
  steps
  {
 echo 'Building'


 sh 'mvn package -Dv=${BUILD_NUMBER}'
 


 }

 }

 stage('Packing war file')

 {
 steps
 {
 echo 'zipping '
 sh 'mv target/*.war /var/lib/jenkins/jobs/PackingwarFile/builds/$BUILD_NUMBER'
 
  dir('/var/lib/jenkins/jobs/PackingwarFile/builds/$BUILD_NUMBER') {
      sh "pwd"}



}

}
 }

 }

