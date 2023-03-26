pipeline{
	agent any 
	stages{
		stage('1-clone'){
			steps{
				checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'git-id', url: 'https://github.com/EtechDevops-Team5/team5App.git']])
			}
		}
		stage('2-systemscheck'){
			steps{
				sh 'sudo systemctl status jenkins'
			}
		}
		stage('3-diskcheck'){
			steps{
				sh 'df -h'
			}
		}
		stage('4-blockcheck'){
			steps{
				sh 'lsblk'
			}
		}
        stage('5-ops-check'){
            steps{
                sh 'cat/etc/os-release'
            }
        }
	}
}