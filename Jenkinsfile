node('ridley') {

    stage('Cloning git') {
        checkout scm
    }

    stage('Setting variables') {
        sh "sed -i 's/SUBATHONTIMER_DB_PASS/${DB_PASS}/' docker-compose.yml"
        sh "sed -i 's/SUBATHONTIMER_TAG/${TAG}/' docker-compose.yml"
    }

    stage('Deploying application') {
        sh "docker compose up -d --build"
    }
}