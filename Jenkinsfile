@Library('yaml-supler') _
import com.lesfurets.jenkins.yaml.dsl.YamlPipeline

def yaml = loadYaml 'vars.yml'

new YamlPipeline()
    .withEnv(yaml)
    .pipeline {
        agent any
        stages {
            stage('Print variables') {
                steps {
                    echo "Var 1: ${env.var1}"
                    echo "Var 2: ${env.var2}"
                    echo "Var 3: ${env.var3}"
                }
            }
        }
    }

