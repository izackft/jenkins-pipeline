stage 'Checkout'
 node('master') {
  deleteDir()
  checkout scm
 }

stage 'Build & Archive Apk'
 node('slave') {
  sh 'export ANDROID_SERIAL=192.168.56.101:5555 ; ./build.sh'
  step([$class: 'ArtifactArchiver', artifacts: 'meu_aplicativo/build/outputs/apk/meu_aplicativo.apk'])
 }
