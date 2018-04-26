stage 'Checkout'
 node('master') {
  deleteDir()
  checkout scm
 }

stage 'Build & Archive Apk'
 node('master') {
  sh 'export ANDROID_SERIAL=192.168.56.101:5555 ; echo "VAAIIIII"'
  step([$class: 'ArtifactArchiver', artifacts: 'meu_aplicativo/build/outputs/apk/meu_aplicativo.apk'])
 }
