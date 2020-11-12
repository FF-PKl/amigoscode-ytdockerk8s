Flow:

  - mongo express request comes via the external service to the mongoExpress pod
  - the mongoExpress pod uses the configMap to send request via the internal service to MongoDB pod
  - the authentication in mongoDB is done via the secrets.

Order of execution

Secret -> mongodb -> configMap -> mongoexpress
