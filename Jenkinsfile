pipeline {
   agent { docker { image 'mcr.microsoft.com/playwright:v1.46.1-jammy' } }
   stages {
       stage(' ') {
         steps {
            sh 'npm i -D @playwright/test'
            sh 'npx playwright install'
         }
      }
      stage(' ') {
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