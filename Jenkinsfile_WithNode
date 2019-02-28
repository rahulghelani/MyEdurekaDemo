timestamps {

node () {

	stage ('Sample_ParentJob - Checkout') {
 	 checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '', url: 'https://github.com/rahulghelani/MyEdurekaDemo.git']]]) 
	}
	stage ('Sample_ParentJob - Build') {
 	
// Unable to convert a build step referring to "hudson.plugins.ws__cleanup.PreBuildCleanup". Please verify and convert manually if required.		// Batch build step
bat """ 
echo "I am Parent" 
 """ 
	}
	stage ('Sample_ChildJob1 - Build') {
 			// Batch build step
bat """ 
echo "I am first child" 
 """ 
	}
	stage ('Sample_ChildJob2 - Build') {
 	
// Unable to convert a build step referring to "hudson.plugins.ws__cleanup.PreBuildCleanup". Please verify and convert manually if required.		// Batch build step
bat """ 
echo "Hello Hero" 
 """ 
	}
}
}
