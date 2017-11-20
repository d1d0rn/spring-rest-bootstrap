#!groovy
stage('build') {
  try{
      timeout(time: 10, unit: 'SECONDS') {
                userInput = input(
                    id: 'Proceed1', message: 'Was this successful?', parameters: [
                    [$class: 'BooleanParameterDefinition', defaultValue: true, description: '', name: 'Please confirm you agree with this']
                    ])
        }
  } catch(err) { // timeout reached or input false
      //def user = err.getCauses()[0].getUser()
      //if('SYSTEM' == user.toString()) { // SYSTEM means timeout.
        userInput = true
      //} else {
        //input false
      //  userInput = false
     // }
  }
  if (userInput == true){
    node{
      sh "echo True"
    }
  }else if (userInput == false){
    node{
      sh "echo False"
    }
  }
}

stage('test') {
    node {
        sh "echo testing"
    }
}


 
