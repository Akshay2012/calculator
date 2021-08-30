pipeline{
    agent{
        label "akshay"
    }
    tools{
        nodejs 'nodejs'
    }
    stages{
            stage("Initialize"){
                steps{
                    sh '''
                        echo "-------executing initialization stage-------"
                        npm install
                    '''
                }
            }
        stage("Test"){
            steps{
                sh '''
                    echo "-------executing testing stage--------"
                    npm run test --watchAll=false
                '''
            }
        }
        stage("Build"){
            steps{
                sh '''
                    echo "------executing build stage--------"
                    npm run build
                '''
            }
        }
    }
}