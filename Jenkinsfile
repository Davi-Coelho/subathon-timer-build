node('ridley') {

    stage('Cloning git') {
        checkout scm
    }

    stage('Deploying application') {
        sh "export SUBATHONTIMER_DB_PASS=${DB_PASS}"
        sh "export SUBATHONTIMER_TAG=${TAG}"
        sh "docker compose up -d --build"
    }
}