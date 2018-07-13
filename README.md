# uipath orchestrator API
 
 Exemple avec node :
 
 ```js
const OrchestratorApiClient = require('./src/orchestrator-api-client')
(...)
let tenant = [ "TenantName", "admin", "password" ]
let user = {
                      "EmailAddress":  "",
                      "Type":  "User",
                      "IsEmailConfirmed":  true,
                      "Password":  "passw0rd",
                      "UserName":  "xld_Uipath",
                      "Surname":  "XL_DEPLOY",
                      "Name":  "XL_DEPLOY",
                      "IsActive":  true,
                      "RolesList":  [
                                        "Administrator"
                                    ]
                  }
let client = new OrchestratorApiClient(
    "http://urlorchestrator.fr",
    undefined,
    {strictSSL: false}
  )
})
(...)
client.authenticate(...tenant).then((token) => {
  client.createUser(user)
    .then(r => console.log(tenant[0] + " : " + user.UserName+" OK"))
    .catch(err => console.log(err))
}).catch( err => console.log(err) )


