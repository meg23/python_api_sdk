<html>
<body>
<h1>Ecobee API Python SDK</h1>
<div>
This project provides a simple python interface to interact with the ecobee Web REST API.
</div>
<div>
<h2>Overview</h2>
<ul>
<li>Manage Tokens Operations like regestering and refreshing</li>
<li>Format boilerplate api requests.</li>
<li>Provide simple functions to perform common api operations</li>
</ul>
<div>
There are two ways to manage your tokens.
<ol>
<li><b>Local File: </b>Read and Write to files on your computer. (refreshes tokens as needed)</li>
<li><b>Database: </b>Read from a database. (refresheds all tokens on a schedule)</li>
</ol>
The main difference between the two token managers is that the Database system supports multiple processes (or machines)<br>
where as the Local File system does not.<br>
If you do not need to have multiple processes the Local Manager is recommended since it is simpler to setup
</div>
</div>
<h2>Install Guide</h2>
<div>
  
<b>Note: lines with $ mean execute this command in bash</b><br>
  
``` bash
Clone the Repository
$ git clone https://github.com/ecobee/python_api_sdk.git

Navigate inside the root directory
$ cd python_api_sdk

Install the Repository
$ pip install .

#Run the interactive enviornment setup
$ python setup_scripts/env_setup.py
```
</div>

<h2>User Guide</h2>
<div>
Note: Bolded Lines with >>> mean execute this command in python
<h3>Adding Users</h3>


``` python
>>> # Create an ApiInterface object
>>> from ebapi.api_interface import ApiInterface
>>> interface = ApiInterface()
>>> 
>>> #Add a user
>>> interface.add_user()
```
This will dispaly the following test:

Enter the PIN '<some 4 digit pin>' into the Add Application window and click Add Application
waiting press enter to continue...

Navigate to www.ecobee.com and login with you username and password<br>
Home (Top right) --> My Apps (Bottom Left) --> Add application (Enter into Text Field)<br>
Hit enter into you python session<br>

This will generate access and refresh tokens
Press Enter To resume execution once 
</div>
</body>
</html>
