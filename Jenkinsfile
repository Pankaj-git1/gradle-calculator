currentBuild.display='Gradle_pipeline#'+currentBuild.number

pipeline {
     agent any
     stages {
          stage("Compile") {
               steps {
                    sh "./gradlew compileJava"
               }
          }
         
		   //stage("Code coverage") {
  //   steps {
         // sh "./gradlew jacocoTestReport"
         // sh "./gradlew jacocoTestCoverageVerification"
     //}z
//}
		  
stage("Package") {
     steps {
          sh "./gradlew build"
     }
}

     }
}
