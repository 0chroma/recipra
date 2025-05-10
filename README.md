# Recipra

/rɪˈsɪppra/
(ree·sip·prah)
[Audio](http://ipa-reader.xyz/?text=r%C9%AA%CB%88s%C9%AAppra)

A modular, decentralized social network for cooperatively run communities

Recipra is an application that allows the layperson to easily start a community that everyone has a part in running. Communities built with Recipra can have chat, voice calls, events, and can even be extended with custom plugins. Recipra doesn't have a concept of moderation teams, making it relatively stress-free to run. They also don't require hosting or servers, making it easy for non-technical people to create a community, and making it free from corporate control and monitization.

![Recipra Mockup](docs/assets/mockup.svg)

## Help Needed

Since this is a fairly ambitious project, it can use as many volunteers as possible! If you think you can help, don't be afraid to reach out! The main component being worked on currently is the data sync tech, called [InductionDB](https://github.com/0chroma/InductionDB)

## FAQ

### Will I be able to post on a personal feed and have an algorithmic timeline, like on other social media?

No, though you'll be able to provide a small profile. Have you ever had a mutual on twitter that you've wanted to talk to, but never knew how to start the conversation? This is exactly the type of scenario Recipra tries to avoid. Social media that acts on the level of the individual often makes us feel more distant from others and pedestalizes a select few. By putting the focus on communities, it puts less pressure on the individual and makes meeting new people less daunting. It also allows someone's success to bring everyone in the group up together, where an individualized approach would lead to a select few snowballing their platform in isolation.

Rather than providing an algorithmic feed of individual people's posts, we'd rather have people post things to a group, which encourages a community to form and encourages prosocial engagement. When posts spiral outside of their intended audiences, as is common with algorithmic communities, often it ends up losing it's intended context and triggers negative reactions from people misunderstanding the content.

People you interact with frequently may appear more often in the group activity summaries, but rather than using algorithms as a solution for *every* problem, we'd rather give people regular suggestions to make it easier to manually curate what you see.

### In groups, often some people are more active than others. How will this be handled?

To avoid more vocal people flooding a group with content, we can provide the community tools to organize this content better, or condense it down to a single item and summarize it. This way quality should be prioritized over raw quantity.

### Why aren't there things like admins and moderators? How will communities stay civil?

Communities that are dependent on authority figures for moderation are often bad for both parties: the moderation team often burns out since it's a stressful and thankless position to be in, and members can often feel unfairly treated if a single moderator abuses their authority. Distributing this responsibility gives everyone ownership over the community: the burden of making a bad decision won't lie on a single person's shoulders and allows the whole community to learn from the experience, and members are incentivized to limit invitations to people who won't cause drama.

Recipra instead sees power as a social engineering vulnerability; if someone has the power to co-opt a group of agreeable, pro-social people, then we need to change it's structure in order to prevent anti-social people from forcing their will upon others, or manipulating the group.

### How will unethical or illegal content be removed?

Because members are the ones who host all the community's content, they are soley responsible for it's distribution. Users consent to viewing and serving the content within the community after accepting an invitation, and can preview a communitiy's content beforehand. Members can decide collectively to have content removed, and can leave the community if they no longer wish to store and serve it's content. This should be compatible with existing legal means of prosecuting offenders and removing illegal content.

There will be a mechanism in place to prevent community discovery from being spammy/innapropriate (tbd)

### How will devices sync data without a server if they can go offline and online regularly?

With a large enough group, the chances of all but one device being offline at any given point should be relatively rare. In the event that it does happen, we can always apply a user's activity retroactively using CRDTs. For 1:1 interactions such as DMs, you can optionally have that data encrypted and replicated to other members' devices for syncing.

### How well will this scale?

There haven't been many large scale applications that have implemented this kind of moderation system without succumbing to hivemind mentality, witch-hunts, and tyranny of the majority in general. Communities will likely work best at smaller scales where everyone knows each other and new members can be properly vetted. Communities will likely work best with 100 or fewer members. For more ambitious efforts, it's probably better to have tools for having multiple communities organize together rather than figuring out how to make the communities themselves larger. From a technical perspective, scaling trustless collaborative applications can also be difficult, though likely not impossible.

### Do you need to host a server to start a community?

No, the community's data is stored and transmitted between devices without the need of a server like you would with a federated service.

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
   - trial-period invites: new users join as guests with liited rights, and members vote to make them a full member after a duration
   - event-based invites: new users attend a public-facing event, and members can vote to extend membership to them if they like them
   - closed invites: member proposes an invitation + community votes/discusses
   - simple vote kick/ban with discussion
   - report-based bans: members can anonymously report a user's behavior, if a member is reported by enough users it triggers a tribunal where the validity of the reports can be discussed and voted on. If they are valid, members can vote on the severity of the consequences.
   - ban appeals: mechanism for removing a ban if there's improved behavior in another community, proof that they've been seeing professional help, etc.
- Voting Systems
  - Simple Majority/two-thirds majority
  - Ranked Choice
  - Consensus
  - Active-members only
  - etc
- Communication
  - video calls
  - text chat
  - embeddable game sdk
- Content
  - wikis (with edit challenging/approval system)
    - Can be used to establish community rules etc
  - media gallery
  - code/file repositories (via git)
  - public content publishing
- Organization
  - task tracking
  - events/meetup planning tools
  - bill splitting or group buy tools
  - community rules (with tools to discuss rules and vote to change them)
  - proposals (with consensus/voting tools)
  - member-provided services directory (like in mutual aid groups)
  - inventory - check-out/check-in (like in a library), trading between groups, history (who helped make/fix it)
  - marketplaces - trade and sell items inside a community
  - funds tracking (like opencollective)
  - unionizing tools (for community land trusts, worker unions, tenant unions etc)
  - [Quorum-based secret sharing](https://en.wikipedia.org/wiki/Shamir%27s_secret_sharing) for unlocking sensitive info for a group ([example](https://iancoleman.io/shamir/))
  - VoIP phone # for the group, first person to pick up will be connected to the call
- Association
  - Tools for for forming federations and allowing collaboration between communities
  - Profit sharing tools, integration with smart contracts?
  - Shared code of conducts, moderation data, etc.
