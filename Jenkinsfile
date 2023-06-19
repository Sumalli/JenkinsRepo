pipeline {
    agent any
      stages {
        stage('Compile') {
            steps {
                echo 'Code Compiling'
                git URL: https://github.com/JenkinsMavenRepo/samplejavaapp.git'
		sh script: '/var/lib/jenkins/jobs/Compile'
            }
        }
         stage('Review') {
            steps {
                echo 'Code Review-pmd:pmd'
                git URL: https://github.com/JenkinsMavenRepo/samplejavaapp.git'
		sh script: '/var/lib/jenkins/jobs/Review'
            }
        }
         stage('UnitTest') {
            steps {
                echo 'JUnit testing-*xml'
                git URL: https://github.com/JenkinsMavenRepo/samplejavaapp.git'
		sh script: '/var/lib/jenkins/jobs/UnitTest'
            }
        }
         stage('Coverage') {
            steps {
                echo 'Code Coverage-Jacoco coverage-*.exec'
                git URL: https://github.com/JenkinsMavenRepo/samplejavaapp.git'
		sh script: '/var/lib/jenkins/jobs/Coverage'
            }
        }
         stage('Package') {
            steps {
                echo 'Creating an Artifact-*.war file'
                git URL: https://github.com/JenkinsMavenRepo/samplejavaapp.git'
		sh script: '/var/lib/jenkins/jobs/Package'
            }
