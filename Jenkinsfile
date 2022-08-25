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
 sh 'mvn install'


 }

 }

 stage('Packing war file')

 {
 steps
 {
 echo 'zipping '

 sh 'cd target'
 sh 'mv *.war /var/lib/jenkins/jobs/PackingwarFile/builds/$BUILD_NUMBER'


}

}
 }

 }

