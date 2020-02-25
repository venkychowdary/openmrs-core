node ('Docker') {

    stage ('scm') {

        git 'https://github.com/venkychowdary/openmrs-core.git'

    }

    stage ('package') {

        sh 'mvn clean package'

    }

    stage ('junit results') {

        junit 'webapp/target/*.xml'

    }

    stage ('archive artifact') {

        junit 'webapp/target/*.war'

    }

    stage ('build sucess') {

        echo 'Venky you done a Great Job'
        
    }
  
}
