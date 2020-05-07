currentBuild.display='Gradle_pipeline#'+currentBuild.number

pipeline
{
agent any
stages
{
  Stage('SCM checkout')
{
steps
{
git branch: 'dev', url: 'https://github.com/Pankaj-git1/gradle-calculator.git'
}
}
stages('Gradle')  
  {
  stage
    {
      steps
      {
      withGradle
        {
        sh'./gradlebuild.sh'
        sh ./gradlew clean'
        sh./gradlew assemble' 
        sh./gradlew buil'
        }
      }
    }
  }
  
  
  
}
}
