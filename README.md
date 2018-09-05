# Flow Responder Service

FlowResponder enables the Admin to build basic chat behavior with Autolaunch Flows

Testing via Apex 
================

```
System.debug((String) FlowResponder.runFlow('eventsignup', '41512345678', null));
System.debug((String) FlowResponder.runFlow('eventsignup', '41512345678', 'Yes'));
System.debug((String) FlowResponder.runFlow('eventsignup', '41512345678', 'Beer Monster'));
```

Testing via CURL
================

```
curl  https://velocity-platform-96-dev-ed.cs66.my.salesforce.com/services/apexrest/flowresponder/eventsignup/41512342323 -X POST -d '{}' -H "Content-Type: application/json" -H "Authorization: Bearer yourtokenhere"
curl  https://velocity-platform-96-dev-ed.cs66.my.salesforce.com/services/apexrest/flowresponder/eventsignup/41512342323 -X POST -d '{ "userResponse": "Yes"}' -H "Content-Type: application/json" -H "Authorization: Bearer yourtokenhere"
curl  https://velocity-platform-96-dev-ed.cs66.my.salesforce.com/services/apexrest/flowresponder/eventsignup/41512342323 -X POST -d '{ "userResponse": "Beer Monster"}' -H "Content-Type: application/json" -H "Authorization: Bearer yourtokenhere"
```