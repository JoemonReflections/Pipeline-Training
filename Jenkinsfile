pipeline {
  agent any
  stages {
    stage ("Checkout"){
      steps{
        echo 'Pulling the code from the dev branch'
      }
    }
    stage ("Build"){
      steps{
        echo 'Building the application from dev branch'
      }
    }
    stage ("Test"){
      steps{
        echo 'Testing the application from dev branch'
      }   
    }
    stage ("Deploy"){
          steps{
            echo 'Deploing the application in dev branch'
          }
    }
    stage ("Internal"){
          steps{
            echo 'Internal Deploing the application in dev branch'
          } 
    }
    stage ("Staging"){
          steps{
            echo 'Staging Deploing the application in dev branch'

          } 
    }
    stage ("Push Notification"){
          steps{
            echo 'Pushing Notifications to Dev Branch'

          } 
    }

}
}

