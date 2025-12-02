It's a [[Power BI]] external tool that help developers to optimize their Dashboard

The following C# code can be pasted in the tool, and then run the tool to identify areas for improvement:
```C#
System.Net.WebClient w = new System.Net.WebClient(); 

string path = System.Environment.GetFolderPath(System.Environment.SpecialFolder.LocalApplicationData);
string url = "https://raw.githubusercontent.com/microsoft/Analysis-Services/master/BestPracticeRules/BPARules.json";
string downloadLoc = path+@"\TabularEditor\BPARules.json";
w.DownloadFile(url, downloadLoc);
```

The developer can auto optimize the Dashboard using this tool