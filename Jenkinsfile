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
	

	
	
	}
}
