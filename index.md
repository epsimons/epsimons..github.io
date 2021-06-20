# Ethan Simons
## CS-499-T5476 Computer Science Capstone 21EW5


### About Me

My name is Ethan Simons and I am a student at [SNHU](https://www.snhu.edu/) in my senior year. I am poised to graduate in two weeks. I have been married since 1995, and my wife and I have three children together. 

### Self Assesment

#### Software Design and Engineering

When it comes to software design, I feel like I am off to a good start. My artifact shows part of what technologies I am capable of utilizing. The artifact uses an object oriented approach so that different functions can be called by other functions.

#### Algorithms and Data Structures

The algorithms and data structures in my artifact are designed by purpose. Every algorithm is in place to allow the manipulation of data, and the various data structures are in place to contain the data that is being worked with.

#### Databases

I chose MongoDB for this project because it is easy to setup with Python. The original design of the artifact did not call for a database, but then again, the government (my former employer) is very restrictive in what technologies can be utilized.

### My Artifact

The artifact I chose is my "gz_to_xz_converter" which I had written during a work project to free up harddrive space. You can find the file [here](https://github.com/epsimons/Python/blob/main/gz_to_xz_converter_V3.0.2.py) among other projects and work. My artifact was chosen because of how well it fit into the criteria of the course. I beleive that everything required can be found in this one artifact. Examples are below:

### Example of Software Design and Engineering
```python
def fileListProcessing(files, queue_of_files):
    logging.debug("Entered fileListProcessing()")
    
    # Puts first lines from all listed files 
    # into a queue. Provides a safe way of 
    # getting the result from several processes.
    
    #print("fileListProcessing") #debugging
    result = []
    for filename in files:
        logging.debug("Entered loop: for filename in files:\nCall to file_to_xz(filename)")
        file_to_xz(filename)
    logging.debug("result = {}".format(result))
```

You can see that from this snippet of code that this is a definition that makes a call to another definition and passes an argument.

### Example of Algorithms and Data Structures

```python
for i in range(threads):
        # Split the source filelist into several sublists.
        
        list_of_files = [files[j] for j in range(len(files)) if j % threads == i]
        logging.debug("[Step 3a] Set list_of_files variable: {}".format(list_of_files))  # debugging
        #print("list_of_files: {}".format(list_of_files)) # debugging
        logging.debug("[Step 3b] if len(list_of_files) > 0:")  # debugging
        if len(list_of_files) > 0:
            thread_process = Process(target=fileListProcessing, args=([list_of_files, queue_of_files]))
            #print("p: {}".format(p)) # debugging
            logging.debug("[Step 3b1] p = {}".format(thread_process))  # debugging
            thread_process.start()
            list_of_thread_procs += [thread_process]
            #print("procs: {}".format(procs)) # debugging
            logging.debug("[Step 3b2] procs = {}".format(list_of_thread_procs))  # debugging
    # Collect the results:
    all_results = []
    for i in range(len(list_of_thread_procs)):
        # Save all results from the queue.
        all_results += queue_of_files.get()
        
    return len(files)
```

You can see that various types of structures exist here. There are variables that contian numbers, objects that hold lists, objects that hold pathway data, and variables to hold descriptions of other variables such as the length of an item.

### Example of Databases
```python
import pymongo 
```
It starts with an import to allow the functionality

```python
# Set up MongoDB
client = pymongo.MongoClient()
clientName = "gz_to_xz_log_records"
collectionName = "gz_to_xz"
timeNow = datetime.datetime.now()

db = client[ clientName ] # makes a test database called "testdb"
col = db[ collectionName ] #makes a collection called "testcol" in the "testdb"

def db_logging_function(data):
    myTime = datetime.datetime.now()
    col.insert_one({"timestamp": myTime,"data":data})

```
This section will set up and prepare the program to be able to save data to the database.
There is a function created so that all I have to do is call it and the data will be saved.
```python
data = "{} process time:".format(file_name, {time.time() - start})
    print(data)
    logging.info(data)
    db_logging_function(data)
```
In this last snippet, you can see that the data to be saved and/or presented is stored in a variable which is then passed to the screen (print), the log file (logging.info), and finally to the database(db_logging_function).

In every portion of the program I also try and use names that make sense so that anyone reading this can tell what something does.
