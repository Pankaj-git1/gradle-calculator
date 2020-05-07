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
stages('Gradle')  
  {
  stage
    {
      steps
      {
      withGradle(gradle: 'Local_Gradle')
        {
            sh'./gradlewbuild' 
        }
      }
    }
  }
  
}  
 
}

