
pipeline {
    agent any
   stages{
       stage('create and print json file'){
           environment{
               def props = '{"body": "the build fails. To see the build result click on following link $BUILD_URL"}'
           }
           steps{
               echo "$BUILD_URL"
               echo "$props"
               sh '''
               curl -u teodik:Teo@27may1979 --insecure "https://github.com/api/repos/teodik/webhook-test/commits/$GIT_COMMIT/comments" -H "Content-Type: application/json" -X POST -d $props 
               '''
           }
       }
   }
}
