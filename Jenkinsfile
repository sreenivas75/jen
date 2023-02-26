node(label: 'flyway') {
        stage('Pull Code') {
            git url :  'git@github.com:sreenivas75/jen.git', branch: 'main'
                script {
                           //env.GIT_TAG = sh (returnStdout: true, script: "git tag --sort version:refname | tail -1").trim()
                          env.GIT_TAG = sh (returnStdout: true, script: "git rev-parse --short HEAD").trim()
                }

        stage('Verifyversion') {
            steps {
              sh 'docker run --rm flyway/flyway 9 version'
            }
        } 
