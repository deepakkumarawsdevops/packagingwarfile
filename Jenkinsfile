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
 sh 'mv target/*.war /var/lib/jenkins/workspace/PackingwarFile/$BUILD_NUMBER'
 
 
  

}

}
 }

 }

