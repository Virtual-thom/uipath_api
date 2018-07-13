# uipath orchestrator API
 
 Exemple avec node :
 
 ```js
const OrchestratorApiClient = require('../src/orchestrator-api-client')
let tenant = [ "TENANT1", "admin", "passw0rd" ]
let client = new OrchestratorApiClient(
   "https://orchestrator.mondomaine.fr/",
   undefined,
   {strictSSL: false}
)

client.authenticate(...tenant).then((token) => {
 client.getUsers()
   .then(r => console.log(r))
   .catch(err => console.log(err))
}).catch( err => console.log(err) )
```

