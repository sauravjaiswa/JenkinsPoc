node('master') {
    stage('Checkout'){
        checkout scm
    }
    stage('Build'){
        sh "sudo systemctl start docker"
        sh "docker build -t jenkinspoc:${BUILD_NUMBER} -f Dockerfile ./JenkinsPoc"
        // sh "docker-compose -f ./docker-compose.integration.yml up"
    }
    // stage 'Pusblish UT Reports'
    //     containerID = sh (
    //         script: "docker run -d jenkinspoc:B${BUILD_NUMBER}", 
    //     returnStdout: true
    //     ).trim()
    //     echo "Container ID is ==> ${containerID}"
    //     sh "docker cp ${containerID}:/TestResults/test_results.xml test_results.xml"
    //     sh "docker stop ${containerID}"
    //     sh "docker rm ${containerID}"
    //     step([$class: 'MSTestPublisher', failOnError: false, testResultsFile: 'test_results.xml'])
}