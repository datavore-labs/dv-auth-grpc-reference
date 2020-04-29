# dv-auth-grpc
The Datavore DvAuth gRPC service allows the datavore product to integrate with thirdparty identity providers. 

This service focuses on authorization and sharing not authentication. Authentication is handled via other means.


## The server
Partners implement the gRPC service server to answer the following 3 calls

+ `resolveUsers` this method allows datavore to display basic information such as email and displayName in our ui when presented with a userId. It also allows us to ask for the groups a user belongs to.
+ `searchUsers` this method allows datavore to provide user search for sharing workbooks and datasources with other users.
+ `searchGroups` this method allows datavore to provide a search for user groups for sharing workbooks and datasources with groups of users.

## The client
The Datavore product implements the gRPC client and makes requests to the thirdparty service

### For more information see
https://grpc.io/

