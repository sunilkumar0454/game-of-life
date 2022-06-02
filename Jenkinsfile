node('JDK8'){

stage('SourcCode') {

    //get the coude from git repo on the branch sprint1_develop

    git branch: 'sprint1_develop', url: 'https://github.com/sunilkumar0454/game-of-life.git'


}

stage('Build the code'){

        sh 'mvn package'

}

stage('Archiveing and Test Results'){

       junit '**/surefire_reports/*.xml'
       archiveArtifacts artifacts: '**/*.war', followSymlinks: false
}

}