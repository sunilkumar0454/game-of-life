pipeline {

    agent{ label 'JDK8'}

    triggers{

        pollSCM('* * * * *')

        
    }

    stages{
           
            stage('SourceCode'){
                   
                    steps{
                       
                       git branch: 'sprint1_develop', url: 'https://github.com/sunilkumar0454/game-of-life.git'

                    }


    }

          stage('Buildsteps'){

              steps{

                  sh 'mvn clean package'

              }
          }

          stage('Archive and Test results')

              { steps{

                 junit '**/surefire_reports/*.xml'
                  archiveArtifacts artifacts: '**/*.war', followSymlinks: false

              }

                  
              }

    }

  
}