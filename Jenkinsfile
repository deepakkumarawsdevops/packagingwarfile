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
 sh 'zip -r Calculator.zip *.war'


}

}
 }

 }

