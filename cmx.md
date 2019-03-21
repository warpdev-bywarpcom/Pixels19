---
layout: default
title: Cisco Connected Mobile Experiences
---
# Cisco Connected Mobile Experiences (CMX)

> Cisco Connected Mobile Experiences (CMX) is a smart Wi-Fi solution that uses the Cisco wireless infrastructure to detect and locate consumers’ mobile devices. With it, your organization can directly deliver content to smartphones and tablets that’s personalized to your visitors’ preferences and pertinent to their real-time indoor locations.
>
> source: [developer.cisco.com](https://developer.cisco.com/site/cmx-mobility-services/)

CMX is powering Pixels, in its On-Premises version.

## CMX On-Premise 
> Use the intelligence in your wireless network. With CMX, view location information, dwell times, and analytics to learn how visitors behave on the site. Our on-premises platform gives you complete control and ownership, and is at the heart of several CMX solutions.
>
> source: [cisco.com](https://www.cisco.com/c/en/us/solutions/enterprise-networks/connected-mobile-experiences/cmx-on-premise.html)

### Features 

CMX offers the following **APIs**:

- **Configuration** - Configure different aspects of MSE.
- **Location** - Find location specific details on visitors.
- **Analytics** - Find analytical data on visitors.
- **Connect** - Find user session information.
- **Presence** - Find presence data on visitors.

Particular note for the Configuration REST APIs where it is possible to subscribe to notifications such as user location change, association and so on.

### Example 

As an example, we can look at integrating with a CRM system when a user connects to the Wi-Fi.
The user arrives and through the captive portal provides its name, e-mail or other information (phone number (verified or not), a specific question) to gain access to the network.

1. Using the Configuration API set a notification to be informed of new associations.
2. Receive a JSON POST notification when a new user joins the Wi-Fi.  
3. Get the information provided by the user using the Connect API.
4. Add the user information to the CRM system, or complement the user profile with this new visit,  using its API.


### Learning

Cisco provides the [Using the Cisco Location Based Services](https://learninglabs.cisco.com/modules/dna-cmx-mse) module on DevNet.

### API Docs

The documentation on the API can be found in [cmxlocationsandbox.cisco.com/apidocs](https://cmxlocationsandbox.cisco.com/apidocs/).

To use the live API test use the following credentials:

- username: ``learning``
- password: ``learning``

## Next step

Pass by our booth and we will provide you with credentials to access the Pixels CMX API!
