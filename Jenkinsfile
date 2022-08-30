pipeline {
  agent any
  stages{
    stage("Nazwa stage\'a"){
      steps{echo "Dzialam"}
    }
    stage("Obliczanie wartosci pi") {
      steps{
        sh  algorithm.sh > report.txt
        archiveArtifacts allowEmptyArchive: true, artifacts: '*txt', fingerprint: true, followSymlinks: false, onlyIfSuccessful: true
      }
    }
  }
}
