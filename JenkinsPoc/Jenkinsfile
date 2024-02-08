node('built-in') {

    stage 'Checkout'
        checkout scm
    stage 'Build'
        sh "docker build -t jenkinspoc:B${BUILD_NUMBER} -f Dockerfile ."
}