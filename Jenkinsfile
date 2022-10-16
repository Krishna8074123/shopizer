pipeline{
    agent any
    triggers { pollSCM ('*/18 * * * *') }
      stages{
        stage ( 'git shopizer' ) {
            steps {
                git url: 'https://github.com/Krishna8074123/shopizer.git',
                branch: 'release'
            }
        }
        stage ( 'package' ) {
            steps {
                sh 'mvn clean install'
            }
        }
    }
}