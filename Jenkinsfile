pipeline{
    agent any
    stage ('build da imagem Docker'){
        steps{
            sh 'docker build -t devops/app .'
        }
    }
    stage('subir docker compose - redis e app'){
        steps{
            sh 'docker-compose up --build -d'
        }
    }
    stage('sleep para subida de containers'){
        steps{
            sh 'sleep 10'
        }
    }
    stagep('teste de aplicação'){
        steps{
            sh 'teste-app.sh'
        }
    }
}