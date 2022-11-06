# What's new in release 1.1 (WidgetApp Administrator guide)

A new Streaming feature is available to add multi-user functionality to WidgetApp. It has two parts.
- **Streaming API (SAPI)**, a function to receive connections from external systems to WidgetApp.
- **Streaming Front End (SFE)**, a function to manage incoming sessions from SAPI.

## Connection to web server
- Connections run over websockets[^1]. Different services[^2] can use the same websocket connection.
## Authentication
- Authentication is unchanged from version 1.0, managed through the existing WidgetApp FrontEnd (WFE).
- SAPI authentication is restricted to authorized user groups, managed with OAuth 2.0 access tokens.
## Session handling
- Legacy API connections are handled by WFE as in version 1.0.
- For new SAPI connections, WFE hands over the connection to SFE. SFE then manages the session in the same way as WFE.
- User actions like *search* or *scrolling* are handled by `_ajax/` endpoints[^3].
## Cautions
- SAPI and SFE processes add to server load. If the system is running slower than expected, see section ___ [^4] for more information on monitoring and restarting stream processes.

## For more information

For more information, see the **Streaming API** section of the **WidgetApp Administrator guide**.

---
***Comments***
- **Purpose**: what is the purpose of SAPI? Is it only to establish multi-user functionality, or are there other benefits? I feel this needs to be clarified to make the documentation more meaningful.
- **Target audience**: technical administrator, focused on the necessary setup, permissions, connections and so on to create a stable environment in which the designer can work with Thing files seamlessly.
- **Content placement in guide structure (Table of Contents, TOC)**: most likely at the top of the document. If there was already a section or table for release 1.0, this would slot in just below.
- **Questions I would ask (potentially more items to document within the Administrator guide)**:
  - Given the target audience, are there no *setup or configuration* steps?
  - As with the User guide, what about error messages or conditions?
  - Changes to functions, database tables etc that will need to be documented within the guide? Possibly user information at least is stored in tables? If not, what sort of static records are used by the Streaming feature?

[^1]: Cross reference to WidgetApps API Guide.
[^2]: Should these services be documented? If so, a link to a section within the Admin guide.
[^3]: Document these? If so, a link to a section within the Admin guide.
[^4]: Link to a section within the Admin guide for the instructions on monitoring and restarting. This content would not be usually included in a **What's new** content section.
