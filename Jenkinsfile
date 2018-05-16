pipeline{
	agent any
	stages{

		stage("Create workspace link")
		{
			def Foldername = JOB_NAME;          
			def theString = "<a href='http://localhost:8080/CodeAnalysisTestPipeline" + Foldername + "/" + BUILD_NUMBER + "/execution/node/3/ws/'>Workspace</a>";
			manager.addShortText(theString, "blue", "white", "0px", "white");
			manager.createSummary("green.gif").appendText("<h1>" + theString + "</h1>", false, false, false, "blue");
		}
		stage('Stage 1')
		{
			steps{
			
				echo 'hello world'
				powershell 'Write-Output "Hello, World, from powershell!"'
				powershell 'C:\\Windows\\Microsoft.NET\\Framework\\v4.0.30319\\MsBuild.exe CodeAnalysisTest.sln /p:RunCodeAnalysis=true'
			
			}

		}
	
	}

}