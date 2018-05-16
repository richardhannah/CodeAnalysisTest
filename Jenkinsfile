pipeline{
	agent any
	stages{
		stage('Stage 1'){
			steps{
			
				echo 'hello world'
				powershell 'Write-Output "Hello, World, from powershell!"'
				powershell 'msbuild CodeAnalysisTest.sln /p:RunCodeAnalysis=true'
			
			}

		}
	
	}

}