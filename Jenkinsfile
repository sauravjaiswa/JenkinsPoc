node('master') {
    stage('Checkout'){
        checkout scm
    }
    stage('Build'){
        // sh "docker build -t jenkinspoc:B${BUILD_NUMBER} -f Dockerfile ."
        sh "docker-compose -f ./docker-compose.integration.yml up"
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