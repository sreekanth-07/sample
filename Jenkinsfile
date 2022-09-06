pipeline {
  agent any
  stages {
    stage('PMD Scan') {
      steps {
        script {
          echo 'test' 
	  bat '''
	  @echo on
          set TOPDIR="%~dp0.."
          set OPTS=
          set MAIN_CLASS=net.sourceforge.pmd.PMD
          echo %PMD_JAVA_OPTS%
          echo "sreekanth"
          java %PMD_JAVA_OPTS% -classpath %TOPDIR%\lib\* %OPTS% %MAIN_CLASS% %*
	  pmd.bat -d src/main -R basic.xml -f text -r log.txt --fail-on-violation false
	  '''
        }
      }
    }
  }
}
