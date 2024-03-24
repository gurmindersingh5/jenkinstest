pipeline {
  agent any
  environment {
    def token = credentials('pat')
  }
stages {
  stage ('check laudi pipeline') {
    steps {
      script {
        sh '''
                echo 'text1' >> text.txt  
                git add text.txt
                git status
                git commit -m 'Updated the text'
                git remote -v
                echo 'made it to here'
                git push https://gurmindersingh5:${token}@github.com/gurmindersingh5/jenkinstest HEAD:main
            '''
    }
  }
}
}
}
