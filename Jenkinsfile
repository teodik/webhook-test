
pipeline {
    agent any
   stages{
       stage('create and print json file'){
           environment{
               def props = """{"body": "the build fails. To see the build result click on following link $BUILD_URL"}"""
           }
           steps{
               echo "$BUILD_URL" + "console"
               echo "$props"
           }
       }
   }
}
