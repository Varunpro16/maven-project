pipeline
{

// agent {
//   label 'DevServer'
// }
agent any

// parameters {
//     choice choices: ['dev', 'prod'], name: 'select_environment'
// }

environment{
    NAME = "piyush"
}
tools {
  maven 'mymaven'
}
stages{
    stage('build')
    {
        steps {
            script{
               echo "this is build stage"  
            }
           
        }
    }
    stage('test')
    { 
        parallel {
            stage('testA')
            {
                steps{
                    echo " This is test A stage"
                }           
            }
            stage('testB')
            {
                steps{
                echo "this is test B stage"
                }
            }
        }
        // post {
        //     success {
        //          dir("webapp/target/"){
        //             stash name: "maven-build", includes: "*.war"
        //          }
        //       }
        //   }

    }

    
   

    
}

}
