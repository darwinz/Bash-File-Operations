# Some Bash commands to make certain file operations easier

Clone this repository, then add the following into your ~/.bashrc :  
`source path/to/file_operations.sh` 

replacing "path/to" with the actual file path to the file_operations.sh file

1. __File Operation commands__
   	- `file_create` - Create a file that contains random contents with a specified size and filepath as prompted by the program
    	- no arguments - user is prompted for required input
    - `encrypt $1` - Encrypt a file using a DES3 hash
    	- __argument $1__ Filepath of file to be encrypted
    	- Usage example: `encrypt file.txt`
    - `decrypt $1` - Decrypt a file that was encrypted using a DES3 hash
    	- __argument $1__ Filepath of file to be decrypted
    	- Usage example:  `decrypt file.txt.des3`
   	- `srch $1 $2` - Search in a specified path for files containing text content specified while ignoring files in .svn and .idea folders
    	- __argument $1__ path to search
    	- __argument $2__ content to search for
    	- Usage example:  `srch . sometext`
    - `cd $@ (override)` - Change directory and list the contents of that directory
    	- __argument $@__ Directory path to cd into
    	- Usage example: `cd somedir`
    - `cdnl` - Change directory without listing contents of that directory
    - `mcd $1` - Make directory with name of $1 argument inside current working directory and cd into that directory
    	- __argument $1__ name of directory to create
    	- Usage example: `mcd newdir`
    - `trash $@` - Move file or directory to Mac OS user's trash
    	- __argument $@__ file or directory to move to trash
    	- Usage example: `trash somefile`
    - `cdf` - Change directory to frontmost window of MacOS Finder
    - `cdpf` - Change directory to frontmost window of MacOS PathFinder 
    - `extract $1` - Extract most known archives with one command
    	- __argument $1__ Filepath to archive to be extracted
    	- Usage example:  `extract archive.tar.gz`
