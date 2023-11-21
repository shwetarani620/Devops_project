pipeline {
  agent any 
   
  stages {
    // stage ('Initialize') {
    //   steps {
    //     sh '''
    //             echo "PATH = ${PATH}"
    //             echo "M2_HOME = ${M2_HOME}"
    //         ''' 
    //   }
    // }
    //     stage ('Check Secrets') {
    //    steps {
    //    sh 'trufflehog3 https://github.com/shwetarani620/Devops_project.git -f json -o truffelhog_output.json || true'
    //    }
    //  }
    //   stage ('Software Composition Analysis') {
    //          steps {
    //              dependencyCheck additionalArguments: ''' 
    //                  -o "./" 
    //                  -s "./"
    //                  -f "ALL" 
    //                  --prettyPrint''', odcInstallation: 'owasp-dc'

    //              dependencyCheckPublisher pattern: 'dependency-check-report.xml'
    //          }
    //      }
   
stage ('Static Analysis') {
      steps {
        withSonarQubeEnv('Sonar') {
          sh 'mvn sonar:sonar'
          // sh 'mvn clean sonar:sonar -Dsonar.java.binaries=src'  
        }
      }
    }
    //  stage ('Generate build') {
    //   steps {
    //     sh 'mvn clean install -DskipTests'
    //   }
    // }  
      
    //   stage ('Deploy to Server Application') {
    //         steps {
    //        sshagent(['server-application']) {
    //           sh 'scp -o StrictHostKeyChecking=no /var/lib/jenkins/workspace/DevSecOps/target/01-maven-web-app.war root@192.168.80.32:/opt/tomcat/webapps/'
    //           sh 'ssh -o  StrictHostKeyChecking=no root@192.168.80.32 "bash /opt/tomcat/bin/shutdown.sh"'
    //           sh 'ssh -o  StrictHostKeyChecking=no root@192.168.80.32 "bash /opt/tomcat/bin/startup.sh"'
    
    //        }
    //        }     
    //     }
    //   stage ('Dynamic analysis') {
    //         steps {
        //    sshagent(['application_server']) {
        //         sh 'ssh -o  StrictHostKeyChecking=no root@192.168.80.32 "sudo docker run --rm -v /home/jenkins:/zap/wrk/:rw -t owasp/zap2docker-stable zap-full-scan.py -t http://192.168.80.32:8080/tomcat -x zap_report || true" '
        //       }
        //    }
        // }
      }
    }  
