# Robocorp Connector
Robocorp is a python-based automation platform (https://robocorp.com/). This connector allows you to interact with your python automations.

# How it works
This connector extends Camunda's rest connector to perform operations in Robocorp. See: https://robocorp.com/api for the API documentation.

# Authentication
Authentication is done through an API key which you can generate through Robocorp control room. In your Camunda model, it is recommended to use a secret.

# Supported operations
- Start process run
- Stop process run
- Get workspace

## Start process run
To start a process in Robocorp you need to provide the Robocorp instance URL, the process ID, and your workspace id (which can be retrieved with the GET workspace operation or through the control room). 
Returned data is stored in the 'output' variable.

## Stop process run
To stop a process run you need to provide the process run ID, and your workspace ID. Additionally you need to set the variables 'set remaining work items as done' and 'terminate activity runs' to true or false. The process run ID can be returned from the Start process run operation. 

## Get workspace
To get the workspace ID, you need to provide your workspace ID, which can also be found through the control room.

# Contact
If you have any questions or want to contribute please contact Rick Balfoort (rick.balfoort@incentro.com) or use Github to reach out.

# Acknowledgements
A special thanks to Raivo at robocorp (https://github.com/raivolink) for giving the first example with his robocorp Camunda demo livestream.
