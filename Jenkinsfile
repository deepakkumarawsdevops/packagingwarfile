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
 dir('target')
 {
 sh 'zip -r Cal$BUILD_NUMBER.zip *.war'
} 
 sh 'mv target/*.war /var/lib/jenkins/jobs/PackingwarFile/builds/$BUILD_NUMBER'

 

 
 
 
  

}

}
 }

 }

