# What's new in release 1.1 - WidgetApp Administrator guide
A new Streaming feature is available to add multi-user functionality to WidgetApp[^1]. It has two parts.
- **Streaming API (SAPI)**, a function to receive connections from external systems to WidgetApp.
- **Streaming Front End (SFE)**, a function to manage incoming sessions from the Streaming API below.

## Connection to web server
- Connections run over websockets. Different services can use the same websocket connection.
## Authentication
- Authentication is unchanged from version 1.0, managed through the existing WidgetApp FrontEnd (WFE).
- SAPI authentication is restricted to authorized user groups, managed with OAuth 2.0 access tokens.
## Session Handling
- Legacy API connections are handled by WFE as in version 1.0.
- For new SAPI connections, WFE hands over the connection to SFE. SFE then manages the session in the same way as WFE 
---
***Comments***
- **Purpose**: what is the purpose of SAPI? Is it only to establish multi-user functionality, or are there other benefits? I feel this needs to be clarified to focus the documentation.
- **Target audience**: technical administrator. They would focus on setup, permissions, connections and generally helping the designer work with Things seamlessly.
- **Content placement in guide structure (Table of Contents, TOC)**: most likely at the top of the document. If there was already a section or table for release 1.0, this would slot in just below.
- **Questions I would ask (potentially more things to document within the Administrator guide)**:
  - Given the target audience, are there no *setup or configuration* steps?
  - As with the User guide, what about error messages or conditions?
  - Changes to functions, database tables etc that will need to be documented within the guide? Possibly user information at least is stored in tables? If not, what sort of static records are used by the Streaming feature?

[^1]: Is this the only purpose of SAPI?
