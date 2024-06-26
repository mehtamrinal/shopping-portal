pipeline{

    agent any

// uncomment the following lines by removing /* and */ to enable
/*    tools{
       maven 'Maven 3.6.3' 
    }
*/    

    tools{
	noejs 'nodejs'
    }

    stages{
        stage('build'){
            steps{
                echo 'this is the build job'
                sh 'npm build'
                sleep 4
            }
        }
        stage('test'){
            steps{
                echo 'this is the test job'
                sh 'npm test'
                sleep 9
            }
        }
        stage('package run'){
            steps{
                echo 'this is the package run job'
                sh 'npm run package'
                sleep 7
            }
        }
    }
    
    post{
        always{
            echo 'this pipeline has completed...'
        }
        
    }
    
}
