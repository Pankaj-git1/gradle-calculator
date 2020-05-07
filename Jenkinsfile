currentBuild.display='Gradle_pipeline#'+currentBuild.number

pipeline
{
agent any
stages
{
  stage('SCM checkout')
{
steps
{
git branch: 'master', url: 'https://github.com/Pankaj-git1/gradle-calculator.git'
}
}
 
  stage("Package") {
     steps {
          sh "./gradlew build"
     }
}
  
}    
 
}

