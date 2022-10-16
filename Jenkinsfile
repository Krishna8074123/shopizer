pipeline{
    agent any
    triggers{
        cron(' * * * * * ')
    }
    stages{
        stage ('git shopizer'){
            steps{
                git url: 'https://github.com/Krishna8074123/shopizer.git',
                branch: 'master'
            }
        }
        stage ('package'){
            steps{
                sh 'mvn package'
            }
        }
    }
}