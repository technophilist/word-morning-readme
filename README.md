# WordMorning - New words. Everyday. Delivered straight to your inbox.
![Screenshot of app](images/word-morning.png)

<p align = "center">
  <img src = "https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white" />
  <img src = "https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white" />
  <img src = "https://img.shields.io/badge/express.js-%23404d59.svg?style=for-the-badge&logo=express&logoColor=%2361DAFB" />
  <img src = "https://img.shields.io/badge/NPM-%23CB3837.svg?style=for-the-badge&logo=npm&logoColor=white" />
  <img src = "https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white" />
  <img src = "https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white" />
</p>
<p align = "center">
<a href="https://www.repostatus.org/#active"><img src="https://www.repostatus.org/badges/latest/active.svg" alt="Project Status: Active – The project has reached a stable, usable state and is being actively developed." /></a>  
</p>

A fully automated daily email newsletter service aimed at improving the vocabulary of new learners of the English language.

## Table of Contents
- [Tech Stack](#tech-stack)
- [AWS Services](#aws-services)
- [Apis](#apis)
- [Notable Features](#notable-features)
- [Source code and Architecture](#source-code-and-architecture)

## Tech Stack
- [Node.js](https://nodejs.org/en)
- [Express.js](https://expressjs.com)
- [TypeScript](https://www.typescriptlang.org)
- [EJS - Embeded JavaScript](https://ejs.co)
- [Express-rate-limit](https://www.npmjs.com/package/express-rate-limit)
- [Jest (ts-jest)](https://www.npmjs.com/package/ts-jest)
- [Twilio SendGrid Node.js sdk](https://sendgrid.com/en-us/solutions/email-api?utm_source=google&utm_medium=cpc&utm_term=twilio%20sendgrid&utm_campaign=SendGrid_G_S_NAMER_Brand_Tier1&cq_plac=&cq_net=g&cq_pos=&cq_med=&cq_plt=gp&gad_source=1)
- [Bad-words](https://www.npmjs.com/package/bad-words)
- [Multer](https://www.npmjs.com/package/multer)
- [Cron](https://www.npmjs.com/package/cron)
- [DotEnv](https://www.npmjs.com/package/dotenv)
- [Helmet.js](https://helmetjs.github.io)
- [Luxon](https://moment.github.io/luxon/#/)
- [Pino / Pino-pretty](https://www.npmjs.com/package/pino)
- [uuid](https://www.npmjs.com/package/uuid)
- [Cloud Firestore](https://firebase.google.com/docs/firestore)
- [Docker](https://www.docker.com)

## AWS Services
- [Elastic Beanstalk](https://aws.amazon.com/elasticbeanstalk/?trk=7251e6b1-d80c-4891-a63f-a6472921f7a3&sc_channel=ps&ef_id=EAIaIQobChMImu-Z1PK6hgMVJVdHAR3mDgDVEAAYASAAEgLmHPD_BwE:G:s&s_kwcid=AL!4422!3!652240143517!p!!g!!what%20is%20elastic%20beanstalk!19870609179!147363462916)
- [Certificate Manager (ACM)](https://aws.amazon.com/certificate-manager/)
- [Route 53](https://aws.amazon.com/route53/)
- [S3](https://aws.amazon.com/pm/serv-s3/?trk=20e04791-939c-4db9-8964-ee54c41bc6ad&sc_channel=ps&ef_id=EAIaIQobChMIk-GfjfO6hgMVbF5HAR2aPwZjEAAYASAAEgIxqPD_BwE:G:s&s_kwcid=AL!4422!3!651751060962!e!!g!!aws%20s3!19852662362!145019251177)

## Apis 
- [DictionaryApi](https://dictionaryapi.dev)
- [RandomWordApi](https://random-word-api.vercel.app)
  
## Notable features
<dl>
  
  <dt>Secure 🔒</dt>
  <dd>The app uses a valid <b> SSL certificate (obtained from AWS ACM)</b> to encrypt the communication between the browser and the server. This ensures that no data can be intercepted and read by someone else while the information is in transit.</dd>

  <dt>One-Click Unsubscribe (RFC 8058) ✅ </dt>
  <dd>The app implementes one-click unsubscribe(RFC8058) to respect users' choice to unsubscribe and to ensure compliance with the mandatory list-unsubscribe requirements enforced in early 2024.</dd>

  <dt>Open Graph tags 🏷️</dt>
  <dd>The app makes use of open graph tags to display beautiful thumbnails when it is shared on social media platforms like Facebook, Twitter, LinkedIn, Slack, and WhatsApp.</dd>

  <dt>User Timezone specific email delivery ✨</dt>
  <dd>The app respects the user's timezone when a mail is scheduled to be sent. This means, the email would be sent at the same time for every user, irrespective of what timezone the user is in. </dd>

  <dt>Attention to tiny details 🪄</dt>
  <dd>
    <ul>
      <li> Clicking the unsubscribe link multiple times won't bombard users with error messages. Instead, they'll see a friendly "Rejoin Us" page, making it easy to resubscribe if they change their mind. </li>
      <li> Rate Limiting is used to ensure that the app is safe from DoS & DDoS attacks - A bespoke webage gets displayed when a user is being rate limited.</li>
      <li> No matter what browser is being used, the app will display a crisp and clear favicon. (Credits : <a href = "https://realfavicongenerator.net"> RealFaviconGenerator</a>).
     </li>
    </ul>
  </dd>
</dl>

## Source code and Architecture
- Files follow the kebab-case file naming convention.
- Architecture (Dataflow) : `app` --forwards requests-> `routers` --respond to requests using-> `controllers (use validations & contain business logic)` --use-> `services`.
- Commit messages follow the [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) specification.

