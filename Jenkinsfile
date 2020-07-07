pipeline{
    agent any
    agent any
    stages {
    stages {
        stage('Build') {
        stage('Upload to AWS') {
            steps {
            steps {
                sh 'echo "Hello World"'
                withAWS(region:'us-west-2', credentials:'aws-static'){
                sh '''
                    s3Upload(file:'index.html', bucket:'vivek.tech.jenkins', path:'/')
                    echo "Multiline shell steps work too"
                }              
                    ls -lah
                '''
            }
            }
        }
        }
    }
    }