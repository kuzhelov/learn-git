All discussion is related to the contents of the .git in a working directory

# Reference Files

**HEAD file** - stores reference to an active branch
  
**./refs/heads directory** - stores branches (one branch per file) where each branch file contains hash of its last commit object


# Object Files 

**./objects directory** - stores repository objects that are grouped by hashes
* each object is stored in its corresponding location in the archived form. Use git cat-file command to view its content.
* each object has one of the following types (in a hierarchical order):
  * **commit** - contains information about a particular commit
  * **tree** - represents monitored files for the particular commit
  * **blob** - represents file content per se
  
# Commands
    
## git cat-file 

Allow to view a content of the object file.  

**git &lt;option&gt; &lt;object-file-hash&gt;**
  
where **&lt;option&gt;** argument could be one of the following: 
    
+ **-p** - detect object type and print its content in a [p]retty format
    
    
