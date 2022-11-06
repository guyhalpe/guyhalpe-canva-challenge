# What's new in release 1.1 (WidgetApp User guide)  

Multiple users can now work together on the same Thing at the same time. You and other designers can now collaborate in real time.

This is made possible by a new Streaming feature, comprised of two parts:
- **Streaming Front End (SFE)**, a function that pushes changes from other collaborating designers to you via the web server[^1].
- **Streaming API (SAPI)**, a function to receive connections from external systems to WidgetApp.

There is no change to the user interface or functionality. Connect to your Thing file, and edit it as you usually do.[^2]

*Note: if you experience authentication or performance issues, contact your System Administrator.*[^3]

## For more information
For more information, see the **Streaming API** section of the **WidgetApp User guide**.

---
***Comments***
- **Purpose**: what's the purpose of SAPI? Is it only to establish multi-user functionality, or are there other benefits? I feel this needs to be clarified to make the documentation more meaningful.
- **Target audience**: non-technical (designer) user, focused on the changes to the user interface and basic functionality - so this is the focus for the content as well. In keeping with that, I wouldn't tell them about potential authentication and server load issues. Is the term *user* acceptable? Some don't like it, so I've used *designer* wherever possible.
- **Content placement in guide structure (Table of Contents, TOC)**: most likely at the top of the document. If there was already a section or table for release 1.0, this would slot in just below.
- **Questions I would ask (potentially more items to document at a designer level)**:
  - I took it that the Streaming feature is mostly transparent to the designer, but is it fully transparent? Would there be progress or performance indicators?
  - If WidgetApp is now moving to a multi-user experience, would there be UI elements (buttons, icons, chat or communication pop-ups) to interact with other users?
  - What about error messages or conditions for user group validation? Did approved user group validation exist before the Streaming feature?

[^1]: Initially I wanted to add something about serving the changes to the designer quickly, perhaps even in *real time*, but then the notes about the potential server load issue seemed to contradict the idea of a speed improvement. This would be good to add, if we could prove it.
[^2]: I would confirm that this is the case. See bullet 2 under **Questions I would ask** above.
[^3]: This would also be confirmed with an SME before including in the documentation. Relates to bullet 3 under **Questions I would ask** above.  
