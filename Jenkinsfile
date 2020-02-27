node {

    stage ('scm') {
        git 'https://github.com/venkychowdary/openmrs-core.git'
    }

    stage ('package') {
        sh 'mvn package'
    }

    stage ('archiving artifact') {
        archiveArtifacts 'webapp/target/*.war'
    }

    stage ('sonaqube scanner') {
        withSonarQubeEnv ('sonarqube') {
            sh 'mvn org.sonarsource.scanner.maven:sonar-maven-plugin:3.2:sonar'
        }
    }

    stage ('build sucess') {
        echo 'Venky you done a Great Job'
    }

}
