---
layout: default
title: Cisco Webex Teams
---
# Cisco Webex Teams

> Cisco Webex Teams is a simple, secure collaboration platform where you can get things done from anywhere in the world. Webex Teams APIs and integrations are key to helping you digitize your business. The self-enabled integrations, bots, and APIs can be easily customized to your existing processes and workstreams.
>
> source: [developer.cisco.com](https://developer.cisco.com/site/spark/)

## Features 

Webex Teams offers the following features:

- **Webex Teams APIs** - From starting team spaces instantly to creating conversational bots.
- **SDKs & Widgets** - Embed video calls in mobile and web apps.

### Webex Teams APIs

Webex APIs use three major types of applications: Integration, Bots, and Guest Issuer. 

When the application is acting on behalf of someone else, integrations is the way to go.  That is why OAuth 2 is the authentication framework, providing a set of scopes that define the required level of access.

Bots are, well, bots. When you are in a meeting, bots look like people and are, in many ways, just like regular users.
They are intended to automate routine tasks and inject contextual content, but what you do with them is only limited by your imagination.
For authentication bots use Tokens.

A significant remark is that bots, when in group rooms, only have access to messages in which they are mentioned (with a ``@bot_name``). 

Lastly, Guest Issuer applications are the way to give guest users temporary access to users within your organization and are usually associated with widgets in a website or application. 

The Guest Issuer can have group and 1:1 spaces with users in your organization without having to log in. These spaces behave like regular spaces, meaning they are persistent.  

The Webex Teams APIs are RESTful and accept either ``application/json`` or ``application/x-www-form-urlencoded`` content types.
For returning data the APIs support JSON.

Bots and Integrations use the following APIs:

- **People** - The registered users of Webex Teams
- **Rooms** - The virtual meeting places
- **Memberships** - Represent the person's relationship to a room
- **Messages** - How we communicate in a room
- **Teams** - Groups of people with a set of rooms
- **Team Memberships** - Represent a person's relationship to a team
- **Webhooks** - Allows your app to be notified (via HTTP) when a specific event occurs
- **Events** - Generated when actions take place

There are other APIs, such as Organizations, Licenses, Roles, and more, but this is mostly for administration and mainly read-only.

Relevant information on this API is their (Cisco) development policy. The product has changed, Rooms are now called Spaces, and Spark is now  Webex Teams. 
Despite that, the API hasn't changed, and as an example, the endpoint to list Webex Teams spaces is ``https://api.ciscospark.com/v1/rooms``. 

### SDKs & Widgets

> Webex Teams SDKs and Webex Teams Widgets provide the easiest way for developers to embed high quality audio-video calling and messaging into any web or native application.
>
> source: [developer.cisco.com](https://developer.webex.com/sdks-and-widgets.html)

We can decompose SDKs & Widgets into three categories: 

- **Widgets** - Web components written in React
- **Web and Mobile SDKs** (IOS, Android, and Browser/JS) - Incorporate Webex Teams features in web and mobile apps
- **Server Side SDKs** (Java, Node.js, and Community) - Helper libraries for bots and integrations with the Webex Teams API


## Examples 

An easy bot example is the enablement of business applications you use daily.
It can be Exchange, Sharepoint, Salesforce, or other (even internal), as long as it also has APIs. 

Imagine you don't have to think about a meeting room every time you create an event. 

1. In Exchange, you create a meeting and add a bot as one of the attendees and ``@spark`` as the location
2. That bot is notified (that he was added to the Webex Teams space) by Webhook API 
3. The bot uses the Messages API to ask for some information and Webhooks to receive notifications when the user answers:
    
    - In which offices will the meeting take place?
    - Do you need Video Conference, Projector or any other specific feature?

3. The bot interacts with Exchange to find an appropriate room that is available
4. The bot changes the venue in Exchange and informs everyone in the Webex Teams Space

This example could even send a message to the back office requesting catering or wi-fi credentials for guests.

Looking at integrations, imagine you work with a ticketing tool.
A new ticket is open and assigned to you, and then the following happens:

1. The ticketing application interacts with Rooms API and creates space. 
2. Then the Memberships API is called and adds all the relevant users to the space.
3. You solve the problem and ask the client, through Webex Teams, if you can close the ticket.
4. The client acknowledges, and the Webhooks API notifies the ticketing application.
5. The ticketing application closes the ticket and publishes a message in the space asking the client for a review.

An easy example of the SDKs are existing corporate applications.
Imagine you work at a hotel, and you have an application that the hotel guests use. 
With the Webex Teams SDKs, you can offer messaging, audio and video calling integrated with your enterprise collaboration applications right from the guest device.

Looking at widgets, you may use it to enable support on your website.
A small widget on the bottom of the page can be used to immediately create a space with your client and someone from the sales or support department.
If you add the traits added by the Webex Teams APIs you may have a bot solving your customer doubts and linking them with the correct person.

In both cases, if you don't want to ask users to login (OAuth), you should use the Guest Issuer authentication.

These are just some examples. Cisco and its partners created real use cases, and you can try some integrations in the [Webex App Hub](https://apphub.webex.com/categories).

## Learning

Cisco provides [Cisco Webex for Developers](https://developer.webex.com/getting-started.html). It consists of documentation, guides, live API tests, SDK downloads, and use cases.

To "get your hands dirty" head on to [Cisco Learning Labs track on Webex APIs](https://learninglabs.cisco.com/tracks/collab-cloud).

Lastly, don't forget to check [Webex App Hub](https://apphub.webex.com) for ready to use integrations. These applications/bots run in the cloud and don't require programming.

## API Docs

The documentation on the API can be found in [developer.webex.com](https://developer.webex.com/).

A curated list of Cisco Webex resources for developers, following the [awesome framework](https://github.com/sindresorhus/awesome), can be found in [GitHub](https://github.com/CiscoDevNet/awesome-webex).
List also available in [Cisco Code Exchange](https://developer.cisco.com/codeexchange/platforms/webex), for those who prefer a web page interface.


## Next Steps

If you wan to use Integration or Bots just go ahead! A free account in webex teams is enough. 

If you are looking at the Guest Issuer pass by our booth and we will provide you a token!
