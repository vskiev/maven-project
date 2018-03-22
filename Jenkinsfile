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
               steps
               {
                 sh 'mvn clean package'
               }
               post{
                   success{
                      sh 'Now Archiving...'
                      archiveArtifacts artifacts: '**/target/*.war', fingerprint: true 
                         }
               }
           }
          

       }
}