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
git branch: 'master', url: 'https://github.com/Pankaj-git1/gradle-calculator.git'
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
        sh'./gradle build.sh'
        sh ./gradlew clean'
        sh./gradlew assemble' 
        sh./gradlew buil'
        }
      }
    }
  }
  
  
  
}
}
