// pipeline {
//     agent any
//     stages {
//     stage('init'){
//       steps {
//          echo "testing"
//            }
//        }
//       stage('Build'){
//         steps {
//           echo "Building"
//             }
//        }
//     stage('Deploy'){
//       steps {
//         echo "code deploy"
//         }
//       }
//     }
// }
pipeline {
 agent any
  
  stages
       {
           stage('Build')
           {
               step
               {
                 sh 'mvn clean package'
               }
               post{
                   success{
                      'Now Archiving...'
                      archiveArtifacts artifacts: '**/target/*.war' 
                   }
               }
           }

           stage('stage 2')
           {
              step
               {
                   
               }
           }

          

       }



}