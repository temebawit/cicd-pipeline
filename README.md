# cicd-pipeline
For a successful build, you will need to replace the ID credits from the docker hub with your own in the LAST stage.

// 'docker_hub_creds_id' —  Credentials Jenkins
                    docker.withRegistry('https://registry.hub.docker.com', '**c7d0b75e-dfc7-4108-a4c6-b7dc0e5af483**') {
