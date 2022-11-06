# What's new in release 1.1 (WidgetApp API guide)  

A new API is available for external connections to the WidgetApp server, and to allow multiple users to work on the same Thing at the same time.  

This is made possible by a new Streaming feature, which has two parts:
- **Streaming API (SAPI)**,  to send and receive connections from external systems to WidgetApp.
- **Streaming Front End (SFE)**, a function that pushes changes from other collaborating designers to the principal user quickly[^1].

Other features of SAPI:
- SAPI runs over websockets. Different services may use the same websocket connection[^2].
- User actions like *search* or *scrolling* are handled by `_ajax/` endpoints[^3].

*Note: SAPI is authorized only for approved user groups, managed through OAuth 2.0 tokens.*

## Configuration

- The external system connects to `wss://www.widgetapp.com/_stream`.
- External systems using SFE listen on port `200` for stream messages from user action APIs, for example:
  - `widgetApp_useraction_refresh()`
  - `widgetApp_useraction_edit()`

## For more information

For more information, see the **Streaming API** section of the **WidgetApp API guide**.

---
***Comments***
- **Purpose**: what is the purpose of SAPI? Is it only to establish multi-user functionality, or are there other benefits? I feel this needs to be clarified to focus the documentation.
- **Target audience**: technical developer user, coding an external application to enable users to connect to WidgetApp's SAPI.
- **Content placement in guide structure (Table of Contents, TOC)**: most likely at the top of the document. If there was already a section or table for release 1.0, this would slot in just below.
- **Questions I would ask (potentially more things to document**:
  - What about API related error messages or conditions? Check and include.

[^1]: Would it actually be quick, if we have potential server load issues? Something to check.
[^2]: As with the Admin guide update, potentially need to document the services and link to the relevant section in the Admin guide.
[^3]: Not sure if Ajax endpoints need to be added here or in the Admin guide, I would check this with an SME and write it up in the appropriate guide. If in the Admin guide, insert a cross-reference.
