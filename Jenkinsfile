currentBuild.display='Gradle_pipeline#'+currentBuild.number

pipeline
{
agen any
	stages
	{
	stage('SCM checkout')
		{
		git branch: 'master', url: 'https://github.com/Pankaj-git1/gradle-calculator.git'
		}
	}
	
        stage('compile code')
		{
			steps{
		withGradle {
			sh'./gradlew clean'
			sh'./gradlew assemble' 
			sh'./gradlew build'
    
		}
			}
		}
	

	
	
	{}
}
