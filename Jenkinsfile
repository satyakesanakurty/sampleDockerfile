pipeline {
    agent any
    parameters
    {
       string(name: 'variable', description: 'a sample var for testing')
    }
    stages {
        stage('Deploy to Dev env') {
            when {
                branch 'dev'
            }
            steps {             
                    sh """
                        if [ ! -Z ${params.variable} ]
                        then
                            echo "you are in dev and you have entered \n var: ${params.variable}"
                        else
                            echo "you have entered nothing"
                        fi
                    """
                
            }
        }
        stage('Deploy to PROD Env') {
            when {
                branch 'master'
            }
            
            steps {
                 sh """
                           
                        if [ ! -Z ${params.variable} ]
                        then
                           echo "you are in master and you have entered \n var: ${params.variable}"
                        else
                            echo "you have entered nothing"
                        fi
                    """
                
            }
            
        }
        
        
    }
}
