1. Hosted by 3CX or 3CX SMB - Small Business

- These are two deployment methods for 3CX, both of which are monitored 24/7, fully supported, cost-effective, and easy to set up
- 3CX SMB is suitable for less than 20 users and a simple installation, while Hosted by 3CX is for installations with up to 120 users and more advanced features

2. Setup your Team

- This involves setting up users, roles, and groups in your PBX system
- A user can have only one role assigned to them, which will be inherited to all the Groups the user is a member of.

- User Role:

- Basic role with the ability to see other users’ presence.

- Receptionist:

- Can override office hours, handle group calls, and perform operations like divert, transfer, pickup, park, and intercom.

- Group Administrator:

- Access to the “Admin” view, can configure call handling, SIP trunks, and WhatsApp. Cannot listen in or barge in.

- Manager:

-  Similar to Receptionist, but with additional admin settings. Can create users, elevate roles, and listen in or barge in.

- Owner:

-  Has all Group Admin and Manager privileges. Can also whisper during calls and elevate others within their group.

- System Administrator:

-  Sees everything across groups and SIP trunks. Cannot barge in or listen in.

- System Owner:

-  Has all System Admin privileges, including barge in, listen in, and viewing reports and recordings (applies to Dedicated instances).

- Groups can have their own office hours, time zones, and languages to allow separate "Call routing"

3. SIP Trunks

- SIP Trunks are essential for enabling external communication through the 3CX system

- Session Initiation Protocol (SIP) trunk 
- the digital counterpart of an analog trunk line

- telephone circuit

- Purpose:

-  Digital telephony connection over the internet.

- Functionality:

- Virtual phone lines for voice, video, and messaging.
- Cost savings based on concurrent calls.
- Scalability and reliability.

- Benefits:

- Cost savings compared to traditional lines.
- Scalability to handle call volume.
- Reliable failover options.
- Supports multimedia communication.

- 3CX supports issues related to Supported SIP Trunks only
- Using 3CX Preferred and Supported SIP Trunks ensures reliable and steady service
- 3CX also supports DID:

- DID - Direct Inward Dialing:

-  A telephony service that allows a company to assign individual numbers to employees without needing separate phone lines for each, connecting to the PBX system

- Setup Example:

-  An organization can rent fewer physical trunk lines from the telco and use DID to manage inbound calls and route them directly to the desired extension.

- DOD - Direct Outward Dialing:

-  A service that enables team members within a PBX system to make outbound calls directly, without going through an operator2.

- Benefits of DID:

- Cost savings,
- time efficiency,
- improved customer experience,
- easy connection to remote workers,
- and the ability to forward calls to mobile apps.

4. IP Phone Provisioning & Apps

- Both 3CX Apps and supported IP Phones can be used, no need to choose
- The user can select either or toggle between them
- 3CX SBC:

- Overview:

- The 3CX Session Border Controller (SBC) is a software service designed for networks with more than 10 phones, facilitating easy connection of IP Phones to a 3CX system in the cloud or on-premise

- Functionality:

-  It consolidates all SIP and RTP VoIP packets from one location, resolving common firewall and networking issues to ensure reliable connectivity to 3CX

- Installation Requirements:

-  A static IP must be assigned to the device running the 3CX SBC, which needs to be operational at all times

- Alternative Solutions:

-  For networks with less than 10 phones, using an SBC-capable IP phone or the 3CX iOS and Android Apps for single remote phones is recommended

- 3CX Web Client :

- Overview:

- The 3CX Web Client is a comprehensive communication tool that allows users to manage calls, view colleague statuses, hold video conferences, and connect via various channels like voice, live chat, WhatsApp, Facebook, and SMS/MMS.

- Getting Started:

- Users can log in using credentials provided in the “Welcome to 3CX” email or by setting a password. The page also guides on installing the Web Client as a Progressive Web App (PWA) for both Google Chrome and Microsoft Edge.

- Call Management:

-  The page details how to make and manage calls, including transferring calls, starting conference calls, recording calls, and switching to video calls.

- Status & Queues:

-  Users can manage their status to indicate availability and set up call forwarding rules, including automatic status switching based on working hours and adding Caller ID exceptions.

5. Call Handling

- IVRs, Ring Groups, and Queues are a basic need of any call centre or customer-facing business
- Instead of having all calls routed to one agent, use Ring Groups or Queues to distribute them amongst a group of agents, based on their availability, skillset, or other criteria
- Office Hours Configuration:

- Set up business open and break times in the “Office hours” section of the 3CX Web Client, applying to the whole team or specific groups.

- Call Routing:

-  Assign a DID number and route calls based on the time received to different destinations like users, voicemail, ring groups, or queues.

- Announcements:

- Record or upload greetings for callers during office, break, or closed hours, with specific instructions for audio format and settings.

- Overrides & Holidays:

- Manage overrides for office hours and configure holidays to handle calls as if the office is closed

- Queue Manager:

- 3CX Call Centre Management:

- The article discusses how 3CX call centre features help managers optimize agent performance and handle customer queries efficiently.

- Live Panel View:

-  Managers can access live data about call queues, including stats on calls waiting, serviced, abandoned, and average wait times.

- Training Tools:

-  3CX includes live and post-conversation training tools for agents, such as listening in, whispering, and barging into calls.

- Performance Reports:

-  The system offers 24 templated reports for retrospective performance analysis, including queue waiting times and agent login history.

6. Messaging

- With 3CX Messaging, you can interact with customers through various messaging channels
- The people contacting you don't even need to be in the same country
- They can send messages when the office is closed, through offline messages
- Live Chat Set-up

- Introduction:

-  The 3CX Live Chat allows direct communication with website visitors through 3CX.

- Step 1:

- Adding Live Chat in 3CX involves logging into the Web Client, setting the destination for messages and calls, and configuring visitor information requirements.

- Step 2:

-  Customization options for the Chat Bubble include styling, messages, and agent appearance settings.

- Step 3:

- Enabling Live Chat on a website requires adding a plugin for WordPress or HTML code for non-WordPress sites.

Need help passing Open Book 3CX Basic Certification : r/3CX - Reddit. [https://www.reddit.com/r/3CX/comments/korjxh/need_help_passing_open_book_3cx_basic/](https://www.reddit.com/r/3CX/comments/korjxh/need_help_passing_open_book_3cx_basic/).

Notes From Doing The 3CX Basic Certification - GitHub. [https://github.com/OlivierLaflamme/3CXBasicNotes](https://github.com/OlivierLaflamme/3CXBasicNotes).