pipeline{
    agent any
    triggers { pollSCM ('* * * * *') }
      stages{
        stage ( 'git shopizer' ) {
            steps {
                git url: 'https://github.com/Krishna8074123/shopizer.git',
                branch: 'Develop'
            }
        }
        stage ( 'package' ) {
            steps {
                sh 'mvn clean install'
            }
        }
    }
}