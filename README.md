## GolosData
The goal of the GolosData project is to make data from the
GOLOS blockchain more accessible to developers, researchers and 3rd party services.

GolosData is currently powered by MongoDB, the most used nosql, and [5th](http://db-engines.com/en/ranking) most popular database solution in the world.
MongoDB comes with a powerful query language, and it allows us to easily accommodate blockchain changes thanks to schema flexibility.

With GolosData, you can query for any kind of information living on the GOLOS blockchain, such as Accounts, Posts, Transactions, Blocks or any kind of Operations.


### Getting Started
I highly recommend [RoboMongo](https://robomongo.org/) as a GUI utility for exploring GolosData.

**Connection Details**
>Host: golosdata.mapala.net    
Port: 27017    
Database: golosdata     
Username: golosdata     
Password: golosdata     


## Deployment
For synchronization, it is recommended to use your own node.

Run:
```
docker run -it -d --restart unless-stopped avral/golosdata-mongo:latest
```

## Configuration
Golosdata now requires MongoDB.

Additional parameters are set via the Docker ENV

**Defaults**
>MONGO_HOST: localhost       
MONGO_PORT: 27017      
MONGO_DB_NAME: golosdata     
DB_USER: ''     
DB_PWD: ''         
GOLOS_NODE: https://ws.golos.io      
WORKER: scrape_operations     

Create a read-only user from createUser.mongo
from mongodb shell when mongo first starts.
