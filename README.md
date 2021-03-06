
![SuperTokens banner](https://raw.githubusercontent.com/supertokens/supertokens-logo/master/images/Artboard%20%E2%80%93%2027%402x.png)

# SuperTokens

<a href="https://supertokens.io/discord">
<img src="https://img.shields.io/discord/603466164219281420.svg?logo=discord"
    alt="chat on Discord"></a>

## Table of Contents
- [🚀 What is SuperTokens?](https://github.com/supertokens/supertokens-core#what-is-supertokens)
    - [Philosophy](https://github.com/supertokens/supertokens-core#philosophy)
    - [Features](https://github.com/supertokens/supertokens-core#features)
    - [Documentation](https://github.com/supertokens/supertokens-core#documentation)
- [🏗️ Architecture](https://github.com/supertokens/supertokens-core#architecture)
- [🔥 SuperTokens vs Others](https://github.com/supertokens/supertokens-core#supertokens-vs-others)
- [💵 How will we make money?](https://github.com/supertokens/supertokens-core#how-will-we-make-money)
    - [Backers](https://github.com/supertokens/supertokens-core#backers)
- [☕ Why Java?](https://github.com/supertokens/supertokens-core#why-java)
- [🛠️ Building from source](https://github.com/supertokens/supertokens-core#building-from-source)
- [👥 Community](https://github.com/supertokens/supertokens-core#community)
    - [Contributors](https://github.com/supertokens/supertokens-core#contributors)
- [👩‍💻 Contributing](https://github.com/supertokens/supertokens-core#contributing)
- [📜 Development history](https://github.com/supertokens/supertokens-core#development-history)
- [📝 License](https://github.com/supertokens/supertokens-core#license)

If you like our project, please :star2: this repository! For feedback, feel free to join our [Discord](https://supertokens.io/discord), or create an issue on this repo

## What is SuperTokens?
SuperTokens is an open core alternative to proprietary login providers like Auth0 or AWS Cognito. We are
 different because we offer:
- Open source: SuperTokens can be used for free, forever, with no limits on the number of users.
- An on-premises deployment so that you control 100% of your user data, using your own database.
- An end to end solution with login, sign ups, user and session management, without all the complexities of OAuth protocols.
- Ease of implementation and higher security.
- Extensibility: Anyone can contribute and make SuperTokens better!

### Philosophy
Authentication directly affects UX, dev experience and security of any app. We believe that
 current solutions are unable to optimise for all three "pillars", leading to a large number of
  applications hand rolling their own auth. This not only leads to security issues, but is also a massive
   time drain.
  
We want to change that - we believe the only way is to provide a solution that has the right level of
 abstraction, gives you maximum control, is secure, and is simple to use - just like if you build it yourself,
  from scratch (minus the time to learn, build and maintain).
  
We also believe in the principle of least vendor lockin. Your having full control of your user's data means that you can switch away from SuperTokens without forcing your existing users to logout, reset their passwords or in the worst case, sign up again. 

### Features
#### ❗⭐❗⭐ We want to make features as decoupled as possible. This means, you can use SuperTokens for just login, or just session management, or both. In fact, we also offer session management integrations with other login providers like Auth0.
- Login (coming soon):
    - A decoupled login & sign up form as React components - pretty by default, but fully customisable.
    - Email & password login with email verification, and forgot password flows
    - Extensibility to build other methods of login - for example passwordless login.
    - Extensibility to chain various login challenges
    - Password management - hashing + salting.
    - Social and other types of login
<img src="https://raw.githubusercontent.com/supertokens/supertokens-logo/master/gifs/login-readme.gif" height="300px"/>

- Session management
    - Create, verify, refresh & revoke sessions.
    - Follows all session best practices like using `httpOnly` cookies.
    - Prevents common session vulnerabilities like session fixation, CSRF or brute force attacks.
    - Detects session hijacking using [rotating refresh tokens](https://youtu.be/6Vzit514kZY?t=547).
    - Optimal time and space complexity - session verifications < 1 MS
    - Automatic JWT signing key rotation, without logging users out
    - Ability to get all sessions given a user ID.
    - Reading session data on the frontend, securely.
    - Manipulation of session and JWT payloads

- User management (coming soon)
    - (Un)banning & deleting users
    - Resetting user passwords
    - Associating users with roles
    - Login identity consolidation (if a user logs in via google and via twitter, with the same email, they are
     treated as the same user).

### Documentation
As of now, we only offer session management.

The docs can be seen [here](https://supertokens.io/docs/community/getting-started/installation)

A short [implementation video](https://www.youtube.com/watch?v=kbC-QzxeZ4s&feature=emb_logo)


## Architecture
Please find a writeup about this in the [wiki section](https://github.com/supertokens/supertokens-core/wiki/SuperTokens-Architecture)

## SuperTokens vs others

Please [contact us](mailto:team@supertokens.io) if any of the information listed below is incorrect.

|                                	|       SuperTokens <img src="https://avatars2.githubusercontent.com/u/50478857?s=200&v=4" alt="Supertokens Logo" width="30" height="30">     	|        Auth0 <img src="https://cdn.auth0.com/website/assets/pages/press/img/auth0-badge-5c9de7e409.svg" alt="Auth0 Logo" width="25" height="25">       	|     AWS Cognito <img src="https://m.media-amazon.com/images/G/01/mobile-apps/dex/login-with-amazon/Cognito-Logo._TTH_.png" alt="Cognito Logo" width="35" height="35">    	|      Keycloak <img src="https://dyltqmyl993wv.cloudfront.net/assets/stacks/keycloak-gatekeeper/img/keycloak-gatekeeper-stack-220x234.png" alt="Keycloak Logo" width="30" height="30">     	|     FusionAuth <img src="https://res-3.cloudinary.com/crunchbase-production/image/upload/c_lpad,h_256,w_256,f_auto,q_auto:eco/zvhuxc69smizw7a9gggx" alt="FusionAuth Logo" width="35" height="35">    	|    Firebase Auth</br> <img src="https://static.dribbble.com/users/528264/screenshots/3140440/firebase_logo.png" alt="Firebase Logo" width="30" height="30">   	|
|----------------------------------------	|:-----------------------:	|:------------------:	|:------------------:	|:------------------:	|:------------------:	|:------------------:	|
| Open source                            	|    :heavy_check_mark:   	|                    	|                    	| :heavy_check_mark: 	|                    	|                    	|
| On-premises                             	|    :heavy_check_mark:   	|         :heavy_check_mark: [1]        	|                    	| :heavy_check_mark: 	| :heavy_check_mark: 	|                    	|
| Managed service                        	|    :heavy_check_mark:   	| :heavy_check_mark: 	| :heavy_check_mark: 	|                    	| :heavy_check_mark: 	| :heavy_check_mark: 	|                    	
| Managed service, with your database    	|       Coming Soon       	|                    	|                    	|                    	|                    	|                    	|                    	
| Use with serverless                    	|    :heavy_check_mark:   	| :heavy_check_mark: 	| :heavy_check_mark: 	|                    	| :heavy_check_mark: 	| :heavy_check_mark: 	|                    	
| Free for unlimited users               	|    :heavy_check_mark:   	|                    	|                    	| :heavy_check_mark: 	| :heavy_check_mark: 	|                    	|
| Ease of configuration                  	|    :heavy_check_mark:   	| :heavy_check_mark: 	|                    	|                    	| :heavy_check_mark: 	|                    	|                    	
| Support for distributed infra          	| :heavy_check_mark:  [2] 	| :heavy_check_mark: 	| :heavy_check_mark: 	|                    	|                    	| :heavy_check_mark: 	|                    	
| Database agnostic                      	|    :heavy_check_mark:   	| :heavy_check_mark: 	| :heavy_check_mark: 	|                    	|                    	| :heavy_check_mark: 	|                    	
| Customisable Login widget              	|       Coming soon       	| :heavy_check_mark: 	| :heavy_check_mark: 	| :heavy_check_mark: 	| :heavy_check_mark: 	| :heavy_check_mark: 	|                    	
| Unlimited Social Login                 	|       Coming soon       	|                    	|                    	| :heavy_check_mark: 	|                    	|                    	|                    	
| Role & Attribute based access  control 	|       Coming Soon       	| :heavy_check_mark: 	| :heavy_check_mark: 	| :heavy_check_mark: 	| :heavy_check_mark: 	| :heavy_check_mark: 	| 
| Sessions using cookies                 	|    :heavy_check_mark:   	|                    	|                    	|                    	|                    	|                    	|                    	
| Session hijacking detection            	|    :heavy_check_mark:   	|    :heavy_check_mark:   	|                    	|                    	|                    	|                    	|                    	
| No cloud lockin                        	|    :heavy_check_mark:   	| :heavy_check_mark: 	|                    	| :heavy_check_mark: 	| :heavy_check_mark: 	|                    	|
| Low feature lockin                        	|    :heavy_check_mark:   	|                    	|                    	|                    	|                    	|                    	|
| Dedicated Support                      	|    :heavy_check_mark:   	| :heavy_check_mark: 	| :heavy_check_mark: 	|                    	| :heavy_check_mark: 	| :heavy_check_mark: 	| 

                 	

[1]: For enterprise version only

[2]: In a paid tier


## How will we make money?
Our philosophy is inspired by Gitlab's buyer-based model and by [Enterprise Ready](http://www.enterpriseready.io/). This means that we intend to monitise on features that are:
- Only required by large or medium sized companies; or features that are
- Targetted towards non technical users of this product;

*It's important to realise that the features we intend to monetise are not necessary for the growth and sustainability of your business (unlike many other alternate solutions). This means that you can have a very large business, with millions of users, and still not have to pay us. However, these features are aimed to increase operational effeciency as your business grows - you don't have to use them, but if you do, you will save lots of time and money :)*

Examples of features that will require a subscription:
- Access control features for the dashboard (for managers and execs)
    - SSO / LDAP / MFA login to the dashboard
    - Roles to restrict access to parts of the dashboard.
    - Creation of custom roles for dashboard operations.
- Healthcheck and uptime monitoring (for IT dept.)
    - Cluster health stats
    - Integration with services like PagerDuty
- Features to make operations easier for customer support agents
    - Login as a user
    - Manually send login OTPs
- Advanced analytics features (for product management & design teams)
    - Sign up form A/B testing
- Advanced security (for compliance and security teams)
    - Detailed audit logs of dashboard and end user actions
    - Encryption of stored information

Outside of the open core model, we will also charge for:
- Hosting of the SuperTokens service on our cloud.
- Completely managing the SuperTokens service on your cloud.
- A commercial license that dictates:
    - Different levels of support
    - Liability agreement
    - Building custom features
    - Backporting updates and security fixes


### Backers
<a href="https://www.ycombinator.com/"><img width="75" src="https://www.ycombinator.com/assets/ycdc/ycombinator-logo-b603b0a270e12b1d42b7cca9d4527a9b206adf8293a77f9f3e8b6cb542fcbfa7.png"></a>


## Why Java?
- Java has a very mature ecosystem. This implies that third party libraries have been battled tested since a very
 long time. This adds an additional security benefit.
- Java's strong type system ensures fewer bugs and easier maintainability. This is especially important when
 many people are expected to work on the same project.
- Ability to dynamically load JARs allows us to distribute only the right database plugin, minimising the final
 Docker image size.

## Building from source
Please see our [wiki](https://github.com/supertokens/supertokens-core/wiki/Building-from-source) for instructions.

## Community
- [Discord](https://supertokens.io/discord)
- [Email](mailto:team@supertokens.io)

If you think this is a project you could use in the future, please :star2: this repository!

### Contributors (across all SuperTokens repositories)
<table>
  <tr>
    <td align="center"><a href="https://github.com/rishabhpoddar"><img src="https://avatars1.githubusercontent.com/u/2976287?s=460&u=d0cf2463df96fbdf1138cf74f88d7cf41415b238&v=4" width="100px;" alt=""/><br /><sub><b>Rishabh Poddar</b></sub></a></td>
    <td align="center"><a href="https://twitter.com/Advait_Ruia"><img src="https://pbs.twimg.com/profile_images/1261970454685900800/ALVzsBQJ_400x400.jpg" width="100px;" alt=""/><br /><sub><b>Advait Ruia</b></sub></a></td>
    <td align="center"><a href="https://github.com/bhumilsarvaiya"><img src="https://avatars2.githubusercontent.com/u/21988812?s=460&u=c0bcde60a8bf1a99baafced55dd1a8d901fa7e4a&v=4" width="100px;" alt=""/><br /><sub><b>Bhumil Sarvaiya</b></sub></a></td>
    <td align="center"><a href="https://github.com/jscyo"><img src="https://i.stack.imgur.com/frlIf.png" width="100px;" alt=""/><br /><sub><b>Joel Coutinho</b></sub></a></td> 
  </tr>
  <tr>
   <td align="center"><a href="https://github.com/RakeshUP"><img src="https://avatars1.githubusercontent.com/u/20946466?s=400&u=01d7d6d701eedd8345e491172e3af04578d18113&v=4" width="100px;" alt=""/><br /><sub><b>Rakesh UP</b></sub></a></td>
   <td align="center"><a href="https://twitter.com/mufassirkazi"><img src="https://i.stack.imgur.com/frlIf.png" width="100px;" alt=""/><br /><sub><b>Mufassir Kazi</b></sub></a></td>
<td align="center"><a href="https://github.com/nkshah2"><img src="https://avatars2.githubusercontent.com/u/18233774?s=400&u=5befa41674cfcd6c6060103360ab323cdfa24dcb&v=4" width="100px;" alt=""/><br /><sub><b>Nemi Shah</b></sub></a></td>
<td align="center"><a href="https://github.com/irohitb"><img src="https://avatars3.githubusercontent.com/u/32276134?s=400&u=0b72f6c4e6cfa749229a8e69ed86acb720a384e7&v=4" width="100px;" alt=""/><br /><sub><b>Rohit Bhatia</b></sub></a></td>
  </tr>
  <tr>
<td align="center"><a href="https://github.com/mmaha"><img src="https://avatars3.githubusercontent.com/u/297517?s=400&u=8c41caf46c511ed2054c3d14c23193eda0d996af&v=4" width="100px;" alt=""/><br /><sub><b>Madhu Mahadevan</b></sub></a></td>
  </tr>
</table>

## Contributing
Please see the [CONTRIBUTING.md](https://github.com/supertokens/supertokens-core/blob/master/CONTRIBUTING.md) file for instructions.

## Development history
Over the last few months, we have built out session management for SuperTokens. During this period, we have made our
 fair share of mistakes:
 - Our first version was architected such that it tightly coupled the backend and database layer. So we had one
  `npm` library for NodeJS with MySQL, and another one for NodeJS with MongoDB etc. When adding support for a new
   backend framework, majority of the logic and tests needed to be rewritten. It became clear that we needed to add a
    service in the middle. We do realise that adding this service means it's harder to get started and that there is
     an extra point of failure, however from the perspective of supporting each tech stack, this decision makes sense, since the failure problem can be addressed through easy to implement technical means.
 
- Until August, 2020, our license was not truly open source. This was done as an experiment to get feedback on the
  importance of software license for the startup community. Since then, it's become very clear that we must use a
   standard open source license, so we chose Apache 2.0
   
- Our community version used to ping our APIs from time to time. This was done for us to understand
 adoption of our session management solution. However, it quickly became clear that that was a bad move.
 
- We used to have a notion of a license key that was required to use the community version. This license key was
 issued by us, and would never expire. Some parts of the code still refer to that, however, it's only for backwards
  compatibility. For all intents and purposes, a license key doesn't exist for this version, which means anyone can build from source, and use SuperTokens for free, forever. 

## License
&copy; 2020 SuperTokens, Inc. All rights reserved.

Licensed under the Apache 2.0 license.
