 pipeline{

 agent any

 stages{

 stage('Checkout'){
  steps{
      git branch: 'main', credentialsId: 'git_crediantials', url: 'https://github.com/laxmiduttasen/jenkins-ansible.git'
       }
 }
 stage('AnsibleExecution'){
  steps{
    ansiblePlaybook credentialsId: 'auser', installation: 'ansible', inventory: 'dhost.inv', playbook: 'ansible.yml', vaultTmpPath: ''
      }
    }
}
}
