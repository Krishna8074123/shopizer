pipeline{
    agent any
    triggers
        { pollSCM ('*/18 * * * *') }
    stages{
        stage ( 'git shopizer' ) {
            steps {
                git url: 'https://github.com/Krishna8074123/shopizer.git',
                branch: 'Develop'
            }
        }
        stage ( 'package' ) {
            steps{
                sh script: 'mvn package'
            }
        }
        stage ( 'archive artifacts' ) {
            steps{
                archive includes: "**/target/*.jar"
            }
        }
        stage ( 'test results' ) {
            steps{
                junit testResults: "**/target/surefire-reports/*.xml"
            }
        }
    }
}