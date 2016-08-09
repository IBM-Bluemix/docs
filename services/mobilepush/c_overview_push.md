---

copyright:
 years: 2015, 2016

---

# About Push Notifications
{: #overview-push}
Last updated: 14 June 2016
{: .last-updated}

Push Notifications is a service that you can use to send notifications to iOS and Android device. Notifications can be targeted to all application users or to a specific set of users and devices using tags. You can administer devices, tags, and subscriptions. You can also use an SDK (software development kit) and Representational State Transfer (REST) application program interface (APIs) to further develop your client applications. 

Push Notification is also available as a Bluemix Dedicated service. For information about Push dedicated service, see [Dedicated Services](../../dedicated/index.html). Note that the Push Notifications monitoring tab does not show analytics data.

The Push Notification service is now OpenWhisk enabled. For more information, see [OpenWhisk](../../openwhisk/index.html).


## Push Notification service process
{: #overview_push_process}

Mobile clients can subscribe and register for the Push Notification service. On startup, mobile applications register and subscribe themselves to the Push Notification service. The notifications are dispatched to the Apple Push Notification Service (APNS) or Google Cloud Messaging (GCM) server and then sent to registered mobile clients.

![Push Overview](images/overview.jpg)


###Mobile applications
{: mobile-applications}

On startup, mobile applications register and subscribe themselves to the Push Notification service to receive notifications.

###Backend applications
{: backend-applications}

Backend applications can be on premises or in a public cloud. Backend applications use the Push Notification service to send context-sensitive notifications to mobile users. The backend applications are not required to maintain and manage mobile devices and user information for sending push notifications. Instead, backend applications can use the Push Notification service.

###App backend owner
{: app-backend-owner}

The role that created the mobile backend application that bundles an instance of the Push Notification service. This person configures and sets up the Push Notification service to suit the backend applications that use the Push Notification service and mobile applications that are the target of push notifications.

###Push Notification service
{: push-notification-service}

The Push Notification service manages all the information that is related to the devices that register for notifications. The service keeps your applications transparent to the technology details of sending notifications to these heterogeneous mobile platforms, handling all of this within.

###Gateways
{: gateways}

Mobile device platform-specific cloud services such as Google Cloud Messaging (GCM) or Apple Push Notification Service (APNS) use the Push Notification service to dispatch notifications to the mobile applications.

###Push Security
{: push-security}

PushNotificatoins APIs are secured by two types of secrets - i) appSecret ii) clientSecret.  The 'appSecret' protects APIs that are typically invoked by backend applications such as the the API to send PushNotifications, the API configure to configure settings.   The'clientSecret' protects APIs that are typically invoked by mobile client applications.  At the present moment there is only one API related to registration of a device with an associated UserId that requires this 'clientSecret'.  All other APIs invoked from mobile clients do not require the clientSecret.  The 'appSecret' and 'clientSecret' are allocated to every service instance at the time of binding an application with PushNotifications service.  Refer to the ReST API documentation for more information on how the secrets are to be passed and for what APIs.

## Push notification types
{: #overview-push-types}

###Broadcast
{: broadcast}

When a mobile application registers itself with the Push Notification service, it can start receiving broadcasts. Broadcast notifications are notification messages that are targeted to all the devices that have the application installed and configured for the Push Notification service. Broadcast notifications are enabled by default with any application that is enabled for push notifications. Any application that is enabled for Push Notification service has a predefined subscription to the Push.ALL tag, which is used by server to broadcast notification messages to all the devices. To send a broadcast notification that uses the REST Push API, ensure that the "target" is an empty JSON file when posting to the messages resource.

###Tag-based notifications
{: tag-based-notifications}

Tag notifications are notification messages that are targeted to all the devices that are subscribed to a particular tag. Tags-based notifications allow segmentation of notifications based on subject areas or topics. Notification recipients can choose to receive notifications only if it is about a subject or topic that is of interest. Therefore, tags-based notification provides a means to segment recipients. This feature enables the ability to define tags and then send and receive messages by tags. A message is targeted to only the devices that are subscribed to a tag. You must first create the tags for the application, set up the tag subscriptions and then initiate the tag-based notifications. To send a tag-based notification that uses the REST API, ensure that the "tagNames" are provided when posting to the message resource.

###Unicast notifications
{: unicast-notifications}

Unicast notifications are notification messages that are targeted to a particular device or user. Unicast notifications targeted to devices do not require any additional setup and are enabled by default when the application is enabled for push notifications.

However, Unicast notifications targeted at users require:

- Associating a user ID with a device at the time of registering the mobile device for push notifications.  


- Authorizing such a user ID registration by passing a 'clientSecret' which is allocated when binding a back-end application to the Push Notifications service. 

Typically a mobile application will first run a authentication cycle where the mobile app user is authenticated against a authentication service [like Mobile Client Access](https://console.ng.bluemix.net/docs/services/mobileaccess/index.html). On successful authentication, the authenticated user ID is then passed into the Push Device Registration API along with a clientSecret. The presence of a clientSecret enforces only authorized association of User IDs with mobile device registrations.
To send a Unicast notifications through REST API, make sure that the deviceIds or userIds are provided when posting to a message resource.

###Platform-based notifications
{: platform-based-notifications}

Notifications can be targeted to reach a particular device platform. For example, a notification can be sent to all the Android users only. To send a platform-based notification that uses the REST API, make sure that the targeted platforms are provided when posting to a message resource. Specify the platforms as an array. The supported platforms are as follows:
* A (Apple)
* G (Google)

## Push Notification message size
{: #push-message-size}

The Push Notification message payload size is dependent on the mediators. 

###iOS
{: ios-message-size}

For iOS 8 and later, the maximum size allowed is 2 kilobytes. Apple Push Notification service does not send notifications that exceeds this limit.

###Android
{: android-message-size}

There are no limitations on the Android platform.