# Recipra

/rɪˈsɪppra/
(ree·sip·prah)
[Audio](http://ipa-reader.xyz/?text=r%C9%AA%CB%88s%C9%AAppra)

A modular, decentralized social network for cooperatively run communities

Recipra is an application that allows the layperson to easily start a community that everyone has a part in running. Communities built with Recipra can have chat, voice calls, events, and can even be extended with custom plugins. Recipra doesn't have a concept of moderation teams, making it relatively stress-free to run. They also don't require hosting or servers, making it easy for non-technical people to create a community, and making it free from corporate control and monitization.

## Help Needed

Since this is a fairly ambitious project, it can use as many volunteers as possible! If you think you can help, don't be afraid to reach out!

## FAQ

### Why aren't there things like admins and moderators? How will communities stay civil?

Communities that are dependent on authority figures for moderation are often bad for both parties: the moderation team often burns out since it's a stressful and thankless position to be in, and members can often feel unfairly treated if a single moderator abuses their authority. Distributing this responsibility gives everyone ownership over the community: the burden of making a bad decision won't lie on a single person's shoulders and allows the whole community to learn from the experience, and members are incentivized to limit invitations to people who won't cause drama.

### How will unethical or illegal content be removed?

Because members are the ones who host all the community's content, they are soley responsible for it's distribution. Users consent to viewing and serving the content within the community after accepting an invitation, and can preview a communitiy's content before accepting an invitation. Members can leave at any time to delete all community data from their devices and cease serving the data. This should be compatible with existing legal means of prosecuting offenders and removing illegal content.

### Do you need to host a server to start a community?

No, the community's data is stored and transmitted between devices without the need of a server like you would with a federated service.

### How do I find new communities?

If the community enables it, they can be shown in a public directory. You'll be able to find communities that are accepting new members, and can search based on interests and location. Alternatively you can be invited by friends who are already members.

## Technical Principals

- Decentralized Identity: Create an identity once on your device, and use it anywhere. There isn't a need to choose a server that hosts your identity like you would with federated solutions.
- Passwordless Login: The application transfers your existing identity to a new device in order to "sign in". You can also keep a backup code in the event that all your devices are lost.
- Data Locality: Community related data is only stored on member devices, and is *not* stored on a global blockchain
- Data Decentralization: Any member's device can serve data to another community member's devices, making the data highly available in the event of a device going offline temporarily. Data will also be available across many physical locations for low-latency access.
- Smartphone Friendly: Devices with limited storage can pull down data from those with ample storage on-demand. Devices with metered connections can set limits to how much data they serve.
- Communal Resources: Group members are incentivized to install the application on devices with reliable, high bandwitdh connections in order to increase the community's capabilities (ie, granting the members higher video call quality)
- Modularity: The application should act only as scaffolding for creating a decentralized community, members should be able to adapt the application for their needs through user-made plugins
- Portability: Needs to work across lots of different hardware, *especially* low-cost or second hand devices. It should be easy to port to different UI toolkits/platforms.

## Plugin Ideas

- Member management
   - open invites
   - approval based invites: users submit a survey + community members vote/discuss
   - trial-period invites: users join as guests and members vote to make them a full member after a duration
   - closed invites: member proposes an invitation + community votes/discusses
   - simple vote kick/ban with discussion
   - report-based bans: members can anonymously report a user's behavior, if a member is reported by enough users it triggers a tribunal where the validity of the reports can be discussed and voted on
- Voting Systems
  - Simple Majority/two-thirds majority
  - Ranked Choice
  - Consensus
  - Active-members only
  - etc
- Communication
  - video calls
  - text chat
- Content
  - wikis
  - files/photos/videos
  - code repositories
  - public content publishing
- Organization
  - task tracking
  - events
  - community rules (with tools to discuss rules and vote to change them)
  - proposals (with consensus/voting tools)
  - member-provided services directory (like in mutual aid groups)
  - inventory - check-out/check-in (like in a library), trading between groups, history (who helped make/fix it)
  - funds tracking (like opencollective)
- Association
  - Tools for setting up agreements between communities
