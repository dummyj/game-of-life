node('HMS && QA'){
    properties([pipelineTriggers([cron('30 * * * 1-5')])])
    stage('VCS'){
    //get the latest git code
    git url: 'https://github.com/aavulasrivani/game-of-life.git',
        branch: 'master'
}
    stage('build') {
        //build the package using maven code
        sh 'mvn clean package'
}
stage('testresults') {
    //publish test results
    junit testresults: 'gameoflife-web/target/surefire-reports/*.xml'
    }

}