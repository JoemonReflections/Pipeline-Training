def gv
pipeline {
  agent any
  tools{
    gradle 'Gradle'
  }
  environment{
    VERS="1.1.1"
  }
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
    stage ("Checking Interval"){
      steps{
        echo 'Checking Interval to Dev Branch'

      } 
    }
    stage ("Building Application"){
      steps{
        echo 'Node npm install'
        nodejs("Node"){
          sh 'npm install'
        }
      } 
    }
    stage ("Building Gradle"){
      steps{
        echo 'Gradle '
      } 
    }
    stage ("Building Master"){
      when{
        expression{
          BRANCH_NAME=="master"
        }
      }
      steps{
        echo 'Building Master Branch'
      } 
    }
    stage ("Building Dev Branch"){
      when{
        expression{
          BRANCH_NAME=="dev"
        }
      }
      steps{
        echo "Building Dev Branch ${VERS}"
      } 
    }
    stage ("Loading Grrovy"){
      steps{
        script{
          gv ="load script.groovy"
        }
        
      } 
    }
    stage ("Running Grrovy"){
      steps{
        script{
          gv.build()
        }
        
      } 
    }

}
}

