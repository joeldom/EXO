
<img title="EXO Logo" alt="EXO Logo" style="display:inline;width:200px;height:200px;" src="https://pbs.twimg.com/profile_images/1948746849994584064/iqWWKOvc_400x400.jpg"><img title="EXO Logo" alt="EXO Logo" style="display:inline;width:auto;height:200px;" src="https://pbs.twimg.com/profile_banners/1948686367573291008/1753445934/1500x500">
# [EXO](https://x.com/ecco_exo)
Working on making things sound, look, and work better. Human designed. AI DevOps & marketing.
```
User Input → AI Agent → Content Review → Multi-Platform Posting
     ↓           ↓            ↓              ↓
 Ideas/Topics → Generated → Human Approval → Twitter + Discord
```
### 7.25 Launch
EXO launch v1 Cross Platform Release servicing account + content post. Read more about timeline integration, automation, data stream benchmark & UX Strategy. `http://bit.ly/46tL4TS`
<img width="679" height="379" alt="EXO Launch-v2" src="https://github.com/user-attachments/assets/aea33a9d-733b-4242-8dd3-4094c80972cc" />
<!--### 7.25 Post Launch-->
<!--<img width="1923" height="1134" alt="join" src="https://github.com/user-attachments/assets/f121c754-4df5-4a91-8610-578b27ec0692" />-->

## Account Init
1. create gmail account
2. sign up for x.com account
   a. claim + confirn username
   b. + profile & banner
   c. register [x.com dev](https://developer.x.com/en/portal/projects/1948798860660260864/apps/31259049/keys)
3. connect & verify X with gmail
   a. create passphrase + keybackups
5. create [github.com/repo](https://github.com/joeldom/exo)
   a. find a way to setup AI agent on a repo
   b. add issue [tracking & bug reporting](https://github.com/users/joeldom/projects/9)
   c. add issues to [Backlog](https://github.com/users/joeldom/projects/9)
   d. setup [deploment actions](https://github.com/joeldom/EXO/actions/new)
7. create [Bitly tracking](bit.ly/46tL4TS) `bit.ly/46tL4TS`
8. create [discord webhook](https://discohook.org/)
   a. `server settings` > `integrations`
9. set tokens persmission + usage [X.com -EXO Dev](https://developer.x.com/en/portal/projects/1948798860660260864/apps)
10. use [Claude](https://claude.ai) to write cron job
11. use [discord.js Doc](https://discord.js.org/) to write to `discord.js` > `exo/lib`
12. pull [twitter-api-v2](https://www.npmjs.com/package/twitter-api-v2) to setup `twitter-api-v2` (Node.js)
    a. [X API v2 authentication mapping](https://docs.x.com/fundamentals/authentication/guides/v2-authentication-mapping)
13. setup *Github Actions* to run scripts and cron
14. test [webhook data payload](https://discord.com/developers/docs/resources/webhook) to Discord
15. create [test page](https://www.gitkraken.com/pricing?source=gitkraken) for fund + follow alerts

## Setup
1. install dependancies
   `npm install`
3. environment setup
   `cp .env.example .env`
```
# AI Service (choose one)
OPENAI_API_KEY=your_openai_api_key
ANTHROPIC_API_KEY=your_anthropic_api_key

# Twitter/X API v2
TWITTER_API_KEY=your_twitter_api_key
TWITTER_API_SECRET=your_twitter_api_secret
TWITTER_ACCESS_TOKEN=your_access_token
TWITTER_ACCESS_TOKEN_SECRET=your_access_token_secret
TWITTER_BEARER_TOKEN=your_bearer_token

# Discord
DISCORD_BOT_TOKEN=your_discord_bot_token
DISCORD_CHANNEL_ID=your_channel_id

# Application Settings
PORT=3000
NODE_ENV=development
```
5. configure API keys

Twitter/X API Setup
   1. Visit developer.twitter.com
   2. Create a new app in your developer dashboard
   3. Generate API keys and access tokens
   4. Ensure your app has Read and Write permissions
   5. Save credentials to your `.env` file
   
Discord Bot Setup
   1. Go to Discord Developer Portal
   2. Create a new application
   3. Navigate to "Bot" section and create a bot
   4. Copy the bot token
   5. Invite bot to your server with "Send Messages" permission
   6. Get your channel ID (Enable Developer Mode → Right-click channel → Copy ID)
   
OpenAI
   1. Visit [OpenAI API](https://platform.openai.com/api-keys)
   2. Create an API key
   3. Add to `.env` file
   
Anthropic
   1. Visit [Anthropic Console](https://console.anthropic.com)
   2. Generate an API key
   3. Add to `.env` file

### Usage
#### Start the App
```
# Development mode with hot reload
npm run dev

# Production mode
npm start
```
---

### Content Workflow
1. Launch CLI
   `npm run create-post`
2. Content collab > provide topic idea
3. Agent Round 1 1st pass
4. Iterate > Refine
5. Review > Schedule > Approve
6. Content arrives > X.com + Discord (channel)

**example 1**
```
$ npm run create-post

🤖 AI Agent: What would you like to post about today?

👤 You: I want to share thoughts about the future of AI development

🤖 AI Agent: Here are some content options:

Option 1: "The future of AI isn't just about smarter models—it's about creating systems that truly understand context and nuance. What excites you most about AI's next chapter? 🧠✨ #AI #FutureTech"

Option 2: "Watching AI evolve from simple chatbots to reasoning partners has been incredible. The next frontier? AI that doesn't just process information, but genuinely collaborates with human creativity 🚀 #AIFuture"

👤 You: I like option 2, but can we make it more conversational?

🤖 AI Curator: How about: "Remember when AI was just autocomplete? Now we're building thinking partners that spark creativity rather than replace it. What's the coolest AI collaboration you've experienced? 💭✨ #AIFuture"

👤 You: Perfect! Let's post it.

✅ Posted to Twitter: [link]
✅ Posted to Discord: [link]
```
**example 2**
```
$ npm run create-post

🤖 AI Curator: What are we making today?

👤 You: I have a some new designs I want to add as options to the Shirts section of the Shopify page

🤖 AI Agent: Here are some content options:

Option 1: "The future of AI isn't just about smarter models—it's about creating systems that truly understand context and nuance. What excites you most about AI's next chapter? 🧠✨ #AI #FutureTech"

Option 2: "Watching AI evolve from simple chatbots to reasoning partners has been incredible. The next frontier? AI that doesn't just process information, but genuinely collaborates with human creativity 🚀 #AIFuture"

👤 You: I like option 2, but can we make it more conversational?

🤖 AI Curator: How about: "Remember when AI was just autocomplete? Now we're building thinking partners that spark creativity rather than replace it. What's the coolest AI collaboration you've experienced? 💭✨ #AIFuture"

👤 You: Perfect! Let's post it.

✅ Posted to Twitter: [link]
✅ Posted to Discord: [link]
```
**Scheduling Posts**
```js
const schedulePost = {
  content: "Your post content",
  scheduledFor: "2024-03-15T10:00:00Z",
  platforms: ["twitter", "discord"]
};
```
**Project Structure**
```
├── src/
│   ├── services/
│   │   ├── ai-service.js      # AI API integration
│   │   ├── twitter-service.js # Twitter posting logic
│   │   └── discord-service.js # Discord posting logic
│   ├── utils/
│   │   ├── content-formatter.js # Platform-specific formatting
│   │   └── validator.js        # Content validation
│   ├── cli/
│   │   └── interactive.js      # CLI interface
│   └── app.js                  # Main application
├── config/
│   └── platforms.js           # Platform configurations
├── logs/
│   └── content-history.json   # Posted content log
├── .env.example
├── package.json
└── README.md
```

<!-- ### refs -->
<!-- <img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/f983bdb8-c5af-4b46-bc4b-e82f9c4f7bb6" /> -->

<!-- ![AKIRA-Comparison-Footage_004](https://github.com/user-attachments/assets/8a230993-3a84-4bc0-b280-c1e24ca65fc6)-->
<!-- ![AKIRA-Comparison-Footage_002](https://github.com/user-attachments/assets/355866b8-34ef-40a4-9533-d7a5e438a107)-->
<!-- ![AKIRA-Comparison-Footage_002](https://github.com/user-attachments/assets/355866b8-34ef-40a4-9533-d7a5e438a107)-->

<!-- ![7_be2ff446-a89a-4092-afce-7dc41f97b435](https://github.com/user-attachments/assets/f62c22f2-b81a-4488-92c2-46bcbe0ab1fa)-->

<!-- ![1_7a7fdfdd-8b70-4261-bda3-809c4e8571fd](https://github.com/user-attachments/assets/9ef54586-1b3e-4366-a03d-51b60d3293a9)-->

<!-- ![F_R77WGWwAANZ9K](https://github.com/user-attachments/assets/32821048-077b-4be1-844b-bfdb1a05e435)-->

<!-- ![513385079_18513251422025529_3357303030026765645_n](https://github.com/user-attachments/assets/8f0dbda1-eec4-46e6-922e-c8b1cc7ed46a)-->

<!-- ![27280-1515191364](https://github.com/user-attachments/assets/f26e95ae-9fb6-44f4-986f-c8dc267c6a28)-->

