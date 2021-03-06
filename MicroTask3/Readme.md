# Microtask 3:
Based on the JSON documents produced by Perceval and its source code, try to answer the following questions:

What is the meaning of the JSON attribute timestamp?

- The timestamp attribute stores the datetime when the item was fetched from the data source.

What is the meaning of the JSON attribute updated_on?

- The updated_on attribute stores the datetime(Unix timestamp) when the item was last updated in the data source.

What is the meaning of the JSON attribute origin?
 - Stores the URL of the data source from which data is fetched 

What is the meaning of the JSON attribute category?
- category attributes include category of items to be fetched from origin
- For example: In GitHub Backend, there are 3 categories, 'issue', 'pull_request', 'repository'.

How many categories do the Git and GitHub backends have?
  -Git has 1 category: 'commit'.
  -Github has 3 categories, 'issue', 'pull_request', 'repository'.

What is the meaning of the JSON attribute uuid?
- stands for universally unique identifier (UUID)
- SHA1 of the concatenation of the values from the list passed as argument to the uuid() function. 
- Example,In git backend, for each commit information fetched uuid will be  SHA-1 Hash of the <origin>:<commit>

What is the meaning of the JSON attribute search_fields?
-  It adds the values of the fields defined in `SEARCH_FIELDS` class attribute with
        their corresponding keys.
- For example, The search_fields for Github backend include metadata, owner, and repo.

What is stored in the attribute data of each JSON document produced by Perceval?
- The information that is extracted from data sources are stored in ```data```
For example in git backend data stores:  Author,AuthorDate,Commit,CommitDate,Signed-off-by,commit,files


Identify the code in charge of dealing with remote APIs and explain its logic.


Which is the folder that stores the archives generated by Perceval?
-  The default archive path is ~/.perceval/archives/
-  --archive-path can be used to specify the archive path 
