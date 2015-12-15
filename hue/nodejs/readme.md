

### rest-api ###

search bridge
- open web browser and go "https://www.meethue.com/api/nupnp" and check bridge ip.
  Then go "http://<bridge ip address>/debug/clip.html" 

register user
- input the following values, push your hue bridge button, and push "POST" in web browser.
  - url: /api
  - message: {"devicetype":"dev_app#dev user"}
  - successful response: 
``` json
[
	{
		"success": {
			"username": "3724298230452e772a4f229e1ced283"
		}
	}
]
```   

ligth status
- input the following values, and push "GET"
  - url: /api/3724298230452e772a4f229e1ced283/lights


turning a light off
- input the following values, and push "PUT"
  - url: /api/3724298230452e772a4f229e1ced283/lights/2/state
  - message: {"on":false}

turing a light on with color set
- input the following values, and push "PUT"
  - url: /api/3724298230452e772a4f229e1ced283/lights/2/state
  - message: {"on":true, "sat":254, "bri":254,"hue":10000}


### Node-hue-api ###

installation 
- install.sh

search bridge
- search.js : use nuphpSearch()

register user

ligth status
``` bash
. env.sh; nodejs ./state.js
```

turning a light off

turning a light on with color set

timezone


Reference
- http://www.developers.meethue.com/documentation/getting-started
- https://github.com/peter-murray/node-hue-api



 

