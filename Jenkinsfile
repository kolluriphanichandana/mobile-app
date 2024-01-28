pipeline
{
agent{label 'linux'}
stages
{
stage{'clean')
{
tools
{
   maven 'maven_3.9.0'
}
 steps{
       sh 'mvn --version'
       sh 'mvn clean'
}
}
stage('compile')
{
tools{
      maven 'maven_3.5.0'
}
steps{
      sh 'mvn --version'
      sh 'mvn compile'
}
}
stage('test')
{  
tools{
maven 'maven_3.9.0'
}
steps
{
  sh 'mvn --version'
  sh 'mvn test'
}
}
post{
sucess{
       echo 'job sucess'
}
fail{
        echo 'job fail'
}
}
}
}
