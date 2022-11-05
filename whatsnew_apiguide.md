# What's new in release 1.1 (WidgetApp API guide)  

A new API is available for external connections to the WidgetApp server, and to allow multiple users to work on the same Thing at the same time.  

This is made possible by a new Streaming feature, which has two parts:
- **Streaming API (SAPI)**,  to send and receive connections from external systems to WidgetApp.
- **Streaming Front End (SFE)**, a function that pushes changes from other collaborating designers to you via the web server to show them to you quickly[^1].

SAPI runs over websockets. Different services may use the same websocket connection[^2]

*Note: SAPI is authorized only for approved user groups, managed through OAuth 2.0 tokens.*[^3]

---
***Comments***
- **Purpose**: what is the purpose of SAPI? Is it only to establish multi-user functionality, or are there other benefits? I feel this needs to be clarified to focus the documentation.
- **Target audience**: non-technical (designer) user, focused on the changes to the user interface and basic functionality - so this is the focus for the content as well. In keeping with that, I wouldn't tell them about potential authentication and server load issues. Is the term *user* acceptable? Some don't like it, so I've used *designer* wherever possible.
- **Content placement in guide structure (Table of Contents, TOC)**: most likely at the top of the document. If there was already a section or table for release 1.0, this would slot in just below.
- **Questions I would ask (potentially more things to document at a designer level)**:
  - I took it that the Streaming feature is mostly transparent to the designer, but is it fully transparent? Would there be progress or performance indicators?
  - If WidgetApp is now moving to a multi-user experience, would there be UI elements (buttons, icons, chat or communication pop-ups) to interact with other users?
  - What about error messages or conditions for user group validation? Did approved user group validation exist before the Streaming feature?

[^1]: Ideally I would like to use the words *real time* here', but being cautious - it may not be possible because of the potential server load issue).
[^2]: I would confirm that this is the case. See bullet 2 under **Questions I would ask** above.
[^3]: This would also be confirmed with an SME before including in the documentation. Relates to bullet 3 under **Questions I would ask** above.  
