pipeline {
    agent {
        label 'docker-node'
    }

    stages {
        stage('git clone gitea') {
           steps {
             sh '''
                rm -rf gitea || true
                git clone https://github.com/alextestuser-bot/gitea
                                    
                '''
           }
        }
    stage('install gitea') {
           steps {
             sh '''
                cd gitea
                docker-compose down
                docker-compose up -d 
               '''
           }
        }   
    }
}
