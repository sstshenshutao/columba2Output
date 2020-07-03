# columba2Output
## use it directly  
Your file should come from http://cc1.cloud-columba.org/  
1. the output file of Columba2: you can read the properties "device", "chipDimension" and "channel" as output data of Columba2.  
2. compiledPackage.json: you can read the properties "$schema" to get a pure json schema which can validate the output of Columba2.  

## use it with UMF IDE  
This is a umf package of the output of columba2.  
The source code is inside the source folder.  
The compiled version is in the top folder.  
To use the package:  
1. visit: https://shen.cloud-columba.org/  
2. click: New Project  
3. change: Change the Simple mode to the UMF mode  
4. Use: 
use the meta link of this package as the validator:  
```
	{
	    "$name": "yourPackage",
	    "$use": [
	        {
	            "$packageName": "columba2.output",
	            "$url": "https://raw.githubusercontent.com/sstshenshutao/columba2Output/master/compiledPackage.json"
	        }
	    ],
	    "columba2.output": { ###  write down the output instances here  ###}
	}
``` 
  
use the meta link of this package as subpackage(build a new package):  
```
	### this is a customized package with "columba2.output" and "columbaS" subpackages, you can click "Download" to download the compiled version.
	{
	    "$name": "yourPackage",
	    "$use": [
	        {
	            "$packageName": "columba2.output",
	            "$url": "https://raw.githubusercontent.com/sstshenshutao/columba2Output/master/compiledPackage.json"
	        },
	        "columbaS"
	    ],
	}
``` 
