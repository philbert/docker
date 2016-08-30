node('master') {
  stage 'Checkout'
  checkout scm

  stage 'Build'
  docker.build('jenkins')

  stage 'Test'
  git url: 'https://github.com/sstephenson/bats.git'
  sh "ls -la .."
  sh "ls -la"
  //sh "bin/bats test/bats.bats"
  sh "bin/bats test/suite.bats"
}
