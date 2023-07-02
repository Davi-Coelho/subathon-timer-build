node('ridley') {

    stage('Cloning git') {
        checkout scm
    }

    stage('Deploying application') {
        sh "export SUBATHONTIMER_DB_PASS=${DB_PASS} | export SUBATHONTIMER_TAG=${TAG} | docker compose up -d --build"
    }
}