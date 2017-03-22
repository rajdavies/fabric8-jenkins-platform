#!/usr/bin/groovy
@Library('github.com/fabric8io/fabric8-pipeline-library@master')
def dummy
clientsNode {
  ws {
    checkout scm
    sh "git remote set-url origin git@github.com:fabric8io/fabric8-maven-dependencies.git"

    mavenUpdateOrganisationDependencies{
      organisation = 'fabric8io'
      repos = 'fabric8-jenkins-workflow-steps,kubernetes-pipeline-plugin'
    }
  }
}
