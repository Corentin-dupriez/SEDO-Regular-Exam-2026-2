pipeline {
    agent any 

    stages {
        stage("Build the app"){
            when {
                expression {
                    return env.GIT_BRANCH == 'origin/main'
                  }
              }
              steps{
                  sh 'dotnet build'
                }
          }
        stage("Run the tests"){
            when {
                expression {
                    return env.GIT_BRANCH == 'origin/main'
                  }
              }
              steps {
                  sh 'dotnet test'
                }
          }
      }
  }
