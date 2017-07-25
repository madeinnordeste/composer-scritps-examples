#composer-scritps-examples

Example to run commands/scripts with [Composer](https://getcomposer.org/)



## Define commands

composer.json

	{
    	"scripts" : {
        	"listFiles" : "ls -la",
	        "createFile" : "echo `date +%Y-%m-%d:%H:%M:%S` > date.txt",
    	    "runAll": [
        	    "@listFiles",
            	"@createFile"
        	]
    	}
	}
	
**runAll** is a alias to run **listFiles** and **createFile** scripts, one after other.


## Runn commands

List files:

	php composer.phar run-script listFiles

Create file:

	php composer.phar run-script createFile
	
Run all:

	php composer.phar run-script runAll
	
	
	

##References:

* [Composer](https://getcomposer.org/)
* [Composer Scripts](https://getcomposer.org/doc/articles/scripts.md/)
* [Automatizando tarefas com composer - Imasters](https://imasters.com.br/desenvolvimento/automatizando-tarefas-com-composer/)
		