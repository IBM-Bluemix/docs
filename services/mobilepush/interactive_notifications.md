---

copyright:
 years: 2015, 2016

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen:.screen}
{:codeblock:.codeblock}

# Interactive notifications
{: #interactive-notifications}
Last updated: 12 December 2016
{: .last-updated}

Interactive notifications allow users to act when a notification arrives without opening the application. When an interactive notification arrives, the device shows the action buttons along with the notification message. Interactive notifications are supported on iOS devices with version 8 and later. If an interactive notification is sent to iOS devices with version earlier than 8, the notification actions are not displayed.

##Sending interactive {{site.data.keyword.mobilepushshort}}


Interactive notification can be sent by using the Push dashboard or by using the [REST API documentation](t_restapi.html).

From the {{site.data.keyword.mobilepushshort}} console: 

1. Under the notification tab in Push dashboard, click **Send Notification**. 
2. Choose your notification recipients and click **Next**. 
3. In the compose notification page, interactive push can be sent by setting the Type to either Default or Mixed and specifying the Category value under Advanced Options tab. To configure the category value on the client, check **Handling interactive {{site.data.keyword.mobilepushshort}}** in native iOS application section.

## Handling interactive {{site.data.keyword.mobilepushshort}} in an iOS application

Complete the steps to receive interactive notifications:

1. Enable the application capability to perform background tasks on receiving the remote notifications. 
1. In the AppDelegate (application: didRegisterForRemoteNotificationsWithDeviceTokenapplication:), set the categories before you set the `deviceToken` on `WLPush Object`.
```
if([application respondsToSelector:@selector(registerUserNotificationSettings:)]){
 UIUserNotificationType userNotificationTypes = UIUserNotificationTypeNone | UIUserNotificationTypeSound | UIUserNotificationTypeAlert | UIUserNotificationTypeBadge;
 UIMutableUserNotificationAction *acceptAction = [[UIMutableUserNotificationAction alloc] init];
 acceptAction.identifier = @"OK";
 acceptAction.title = @"OK";
 UIMutableUserNotificationAction *rejetAction = [[UIMutableUserNotificationAction alloc] init];
 rejetAction.identifier = @"NOK";
 rejetAction.title = @"NOK";
 UIMutableUserNotificationCategory *cateogory = [[UIMutableUserNotificationCategory alloc] init];
 cateogory.identifier = @"poll";
 [cateogory setActions:@[acceptAction,rejetAction] forContext:UIUserNotificationActionContextDefault];
 [cateogory setActions:@[acceptAction,rejetAction] forContext:UIUserNotificationActionContextMinimal];
 NSSet *catgories = [NSSet setWithObject:cateogory];
 [application registerUserNotificationSettings:[UIUserNotificationSettings settingsForTypes:userNotificationTypes categories:catgories]];
}
```
	{: codeblock}

1. Implement new callback method on AppDelegate:
	```
	 -(void)application:(UIApplication *)application handleActionWithIdentifier:(NSString *)identifier forRemoteNotification:(NSDictionary *)userInfo completionHandler:(void (ˆ)())completionHandler
	```
	{: codeblock} 
5. This new callback method is invoked when user clicks the action button. The implementation of this method must perform tasks associated with the specified identifier and execute the block in the `completionHandler` parameter.