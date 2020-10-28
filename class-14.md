## Access Control (ACL)

### Review, Research, and Discussion

**When is Basic Authorization used vs. Bearer Authorization?**
_The basis Auth allow you to access the API directly with your credential : user/password._

_To access the API with a bearer token you will need to make 2 call :_

- one to get the bearer token
- one to get the data
  _Once you have the bearer token you can reuse it and keep it for up to 60 minutes. You can refresh (to extend the validity) or revoke the bearer (to remove the validity) if needed._

**What does the JSON Web Token package do?**
_Transmitting information as a JSON object. It is can be signed with a secret, whcih certifies that the only owner of the secret is the party the signed the JWT._
**What considerations should we make when creating and storing a SECRET?**

- Use encryption to store secrets within .git repositories
- Use environment variables
- Use "Secrets as a service" solutions

### Vocabulary Terms

- **encryption**:_process that encodes a message or file so that it can be only be read by certain people._
- **bearer**:_is an HTTP authentication scheme that involves security tokens called bearer tokens. The name “Bearer authentication” can be understood as “give access to the bearer of this token._
- **secret**: _is private to you which means you will never reveal that to the public or inject inside the JWT token._
- **JSON Web Token**:_is a compact URL-safe means of representing claims to be transferred between two parties._

### Preparation Materials

### RBAC

_RBAC is nothing more than the idea of assigning system access to users based on their role within an organization. The system needs of a given workforce are analyzed, with users grouped into roles based on common job responsibilities and system access needs. Access is then assigned to each person based strictly on their role assignment. With tight adherence to access requirements established for each role, access management becomes much easier._

### Access control lists (ACL)

_An ACL is a means of defining access rights by a given user or user group, to a specific object, such as a document. As a simple example, an ACL could be used to allow users from one department to make changes to a document, while only allowing users from other departments to read the document._
