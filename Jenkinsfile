stage 'Build'
node {
  echo "Building stuff"
  stash includes: 'target/my-output-artifact.whatever', name: 'built'
}

input 'Continue to deploy stage?'

stage 'Deploy'
node {
  unstash 'built'
  echo "Deploying stuff"
}
