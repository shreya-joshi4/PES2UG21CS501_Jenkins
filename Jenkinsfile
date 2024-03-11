pipeline{
    agent any
    stages{
        // stage('Clone repository'){
        //     steps{
        //         checkout([$class: 'GitSCM',
        //         branches:[[name: '*/shreya']],
        //         userRemoteConfigs: [[url:'https://github.com/shreya-joshi4/pes2ug21cs501_Jenkins.git']]])
                
                
        //     }
        // }
        stage('Build'){
            steps{
                build 'PES2UG21CS501-1'
                sh 'g++ pipeline_file.cpp -o objectfile'
            }
        }
        stage('Test'){
            steps{
                sh './objectfile'
            }
        }
        stage('Deploy'){
            steps{
                echo 'deploy'
            }
        }
        post{
            failure{
                error 'Pipeline has failed'
            }
        }
    }
}
