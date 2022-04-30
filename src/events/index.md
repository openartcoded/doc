# Events

You can subscribe to the artemis topic `backend-event` (that name can be overrided with property `EVENT_TOPIC_PUBLISH` ) in order to
consume events produced by the main monolith. 

Depending on the [protocol](https://activemq.apache.org/components/artemis/documentation/latest/protocols-interoperability.html) you choose to connect to artemis, you may have the ability to know what's the type of the event received
using the header `EventType`. This can be handy to ease filtering on the events you're not interested in.


In order to be able to download the different attachments, you must create a new service account on keycloak with role `SERVICE_ACCOUNT_DOWNLOAD`.

From your docker container, you can then make api calls to `http://api-backend/api/download` using your oauth secret key.

