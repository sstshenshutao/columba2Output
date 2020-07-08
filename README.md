# columba2Output

## The output file of Columba2  
Your file should come from http://cc1.cloud-columba.org/  
### use it with IDE:  
1. visit: https://shen.cloud-columba.org/  
2. click: New Project  
3. change: Change the Simple mode to the UMF mode  
4. copy the output file of Columba2 to the text box  
### use it directly:  
1. the output file of Columba2: you can get the path "#/columba2.output" (json-pointer(rfc6901)) as the output data of Columba2.  
2. compiledPackage.json: you can read the properties "$schema" to get a pure json schema which can validate the output data of Columba2.  

## The umf package  
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
