pipeline{
	agent any
	stages{
		stage('Stage 1'){
			steps{
			
				echo 'hello world'
				powershell 'Write-Output "Hello, World, from powershell!"'
				powershell 'C:\\Windows\\Microsoft.NET\\Framework\\v4.0.30319\\MsBuild.exe CodeAnalysisTest.sln /p:RunCodeAnalysis=true'
			
			}

		}
	
	}

}