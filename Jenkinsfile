currentBuild.display='Gradle_pipeline#'+currentBuild.number

pipeline {
	
	node() {
    def xml = readFile "${env.WORKSPACE}/Qualitycheck.xml"
    def rootNode = new XmlParser().parseText(xml)
    print Double.parseDouble(rootNode.value()[0].value()[0].value()[0])
    // Next line if position isnt fixed, can return an array
    // if theres more than 1 with structure "Safety.score", [0] at the end takes the first.
    print Double.parseDouble(rootNode.find{it.name() == "Safety"}.value().find{it.name() == "score"}.value()[0])
}
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
