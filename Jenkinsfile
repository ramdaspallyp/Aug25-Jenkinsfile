node{
    stage('scm') {
    git 'https://github.com/ramdaspallyp/game-of-life.git'
    }   
    stage('build stage') {
    sh label: '', script: 'mvn package'
    }
    stage('archive artifact') {
    archive 'gameoflife-web/target/gameoflife.war'
    }
    stage('jUnit results') {
    junit 'gameoflife-web/target/surefire-reports/*.xml'
}
}