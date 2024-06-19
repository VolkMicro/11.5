pipeline {
    agent any
    triggers {
        githubPush()
    }
    stages {
        stage('Run SQL Script') {
            steps {
                script {
                    def dbHost = 'mysql-rfam-public.ebi.ac.uk'
                    def dbPort = '4497'
                    def dbName = 'Rfam'
                    def dbUser = 'rfamro'
                    def sqlFile = 'path/to/your/sql_script.sql'
                    
                    sh "mysql --user=${dbUser} --host=${dbHost} --port=${dbPort} --database=${dbName} < ${sqlFile}"
                }
            }
        }
    }
}
