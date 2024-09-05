pipeline {
   agent any
   stages {
       stage('Installations') {
         steps {
            sh 'npm i -D @playwright/test'
            sh 'npx playwright install'
         }
      }
      stage('help') {
         steps {
            sh 'npx playwright test --help'
         }
      }
       stage('e2e-tests') {
         steps {
            sh 'npx playwright test --list'
            sh 'npx playwright test'
         }
      }
   }
}