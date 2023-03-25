@Library('my-shared-library') _
def yamlFile = "playbook-vars.yml"
def yaml = readYaml(yamlFile)
def extraVars = "supler vars=\"${yaml}\" silent=true"

pipeline {
  agent any
  
  stages {
    stage('Run Ansible Playbook') {
      steps {
        sh "ansible-playbook playbook.yml --extra-vars '${extraVars}'"
      }
    }
  }
}
