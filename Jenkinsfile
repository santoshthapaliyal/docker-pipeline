node {
    environment {
        dockerhub=credentials('dockerhub')
    }
    checkout scm

    docker.withRegistry('https://registry.hub.docker.com', 'dockerhub') {

        def customImage = docker.build("santoshprasad/dockerwebapp")

        /* Push the container to the custom Registry */
        customImage.push()
    }
}
