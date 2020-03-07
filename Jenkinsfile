pipeline {
   agent any

   stages {
      stage('scm') {
         steps {
            git 'https://github.com/devopsprabha/sample.git'
         }
      }
      stage('build') {
         steps {
            bat label: '', script: 'mvn clean'
            bat label: '', script: 'mvn install'
         }
      }
       stage('Deployment') {
         steps {bat label: '', script: 'xcopy /y "C:\\Program Files (x86)\\Jenkins\\workspace\\pro-boy\\target\\a2z-cs.war" "C:\\Program Files (x86)\\Apache Software Foundation\\Tomcat 9.0\\webapps"'
             }
      }
   }
}
