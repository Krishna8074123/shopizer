pipeline{
    agent any
    triggers{
        cron('* */18 * * *')
    }
    stages{
        stage ( 'git shopizer' ) {
            steps{
                git url: 'https://github.com/Krishna8074123/shopizer.git',
                branch: 'Develop'
            }
        }
        stage ( 'package' ) {
            steps{
                sh 'mvn package'
            }
        }
    }
}