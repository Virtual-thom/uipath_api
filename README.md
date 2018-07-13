﻿# uipath orchestrator API
 
 Exemple avec node :
 
 ```js
const OrchestratorApiClient = require('./src/orchestrator-api-client')
(...)
let tenant = [ "TenantName", "admin", "password" ]
let client = new OrchestratorApiClient(
    "http://urlorchestrator.fr",
    undefined,
    {strictSSL: false}
  )
})
(...)
client.authenticate(...tenant).then((token) => {
  client[tenant[0]].createUser(user)
    .then((r) => {
      console.log(tenant[0] + " : " + user.UserName+" OK")
    })
    .catch((err) => {
      console.log(err)
     })
  })
}).catch( err => console.log(err) )


