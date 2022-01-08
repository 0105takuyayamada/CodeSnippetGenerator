# Overview
I created a website that allows you to easily create code snippets for Visual Studio.

# Usage

Items marked with * are required.
  
|Item|Explanation|
|-|-|
|Title*|Name of the code snippet|
|Shortcut*|string that calls the code snippet|
|Author|name of the author|
|Language*|language|
|Imports| Namespace to add. Examples : "System", "UnityEngine"|
|Code|Code|
|Declarations|Details of substitution parameters|

Press Download to download the .snippet file.
Note that if you do not fill in the required fields or write Declarations incorrectly, you will get a snippet file that will not work properly.

## How to write Declarations
You can set the detailed information of the replacement parameter (Examples : $value$) written in Code.

|Item|Description|
|-|-|
|Literal*|name of the parameter|
|Default|Initial value of the parameter|
|Tooltip|description of the parameter|

When you set the next parameter, please start a new line twice.
