pipeline {
     agent any
     stages {
         stage('Upload to AWS') {
             steps {
                 sh '''
                     echo "Uploading to AWS"
                     withAWS(region:'us-west-2', credentials:'aws-static') {
                         s3Upload(file:'index.html', bucket:'myudacity-jenkins-pipeline', path:'https://myudacity-jenkins-pipeline.s3-us-west-2.amazonaws.com/index.html')
                     }
                 '''
             }
         }
     }
}
