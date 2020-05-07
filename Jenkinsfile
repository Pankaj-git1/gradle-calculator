currentBuild.display='Gradle_pipeline#'+currentBuild.number

pipeline
{
agent any
stages('SCM checkout')
{
steps
{
git branch: 'dev', url: 'https://github.com/Pankaj-git1/gradle-calculator.git'
}
}
}
