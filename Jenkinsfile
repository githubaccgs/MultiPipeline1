pipeline {
    agent any 
        tools {
        gradle 'Default'
        //docker {
        //    image 'node:6-alpine'
        //   args '-p 3000:3000 -p 5000:5000'
        //}
        }
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                   echo ".......inside build phase............"
            }
        }
        stage('Test') {
            steps {
                   echo ".......inside test phase............"
            }
        }
        stage('Deliver for development') {
            when {
                branch 'development' 
                 // echo ".......inside branch development ............"
                 // sh (" chmod +x testscript.sh ")
                 // sh ("./testscript.sh")
            }
            steps {
                   echo ".......inside branch development and steps xxxxxx ............"
                   sh (" chmod +x testscript.sh ")
                   sh ("./testscript.sh")
            }
        }
        stage('Deploy for production') {
            when {
                 branch 'production' 
                // echo ".......inside branch production ............"
            }
            steps {
                  echo ".......inside production branch and steps xxxxxx ............"
            }
        }
    }
}
