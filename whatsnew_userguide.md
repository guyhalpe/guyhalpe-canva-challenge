# What's new in release 1.1 - WidgetApp user guide

Designing Things is now collaborative. You and other designers can now work on the same Things file at the same time.

This is made possible by a new Streaming feature, comprised of two parts:
- **Streaming Front End (SFE)**, a function distributes modifications from other collaborating designers to show them to you ([^1]) ([^1]:Ideally I would like to use 'real time here', but this would need to be verified - it may not be possible because of the potential server load issue).
- **Streaming API (SAPI)**, a function to receive connections from external systems to WidgetApp.

---
***Comments***
- Target audience: non-technical (designer) user, focused on the changes to the user interface and basic functionality - so this is the focus for the content as well. In keeping with that, I wouldn't tell them about potential authentication and server load issues.
- Content placement in guide structure (Table of Contents, TOC): most likely at the top of the document. If there was already a section or table for release 1.0, this would slot in just below.
- Questions I would ask (potentially more things to document at a user level):
  - I took it that the Streaming service is mostly transparent to the designer user, but is it fully transparent? Would there be progress or performance indicators?
  - If WidgetApp is now moving to a multi-user experience, would there be UI elements (buttons, icons, chat or communication pop-ups) to interact with other users?
  - What about error messages or conditions for user group validation? Did approved user group validation exist before the 

