node(label: 'flyway') {
        stage('Pull Code') {
            git url :  'https://github.com/sreenivas75/jen.git', branch: 'main'
                        }
        stage('Verifyversion') {
            steps {
              sh 'docker run --rm flyway/flyway 9 version'
            }
        }   
      
}
