---

copyright:
  years: 2015, 2016

---

{:new_window: target="\_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}

# External service integrations
{: #ref-index}
Last updated: 26 September 2016
{: .last-updated}

External service integration allows you to access data and operations from third-party or external services within your {{site.data.keyword.iot_full}} organization.

## Jasper
{: #jasper}

Jasper is an administration and management platform for SIM devices. Jasper is integrated into the {{site.data.keyword.iot_short_notm}} dashboard, making it possible to administer Jasper devices through your {{site.data.keyword.iot_short_notm}} organization dashboard.

### Supported operations for Jasper

The built-in Jasper integration that is provided by our platform provides support for the following Jasper operations:

- View overall Jasper data
  - Shows: Status, Rate Plan, month-to-date data usage, month-to-date SMS usage, month-to-date voice usage, overage limits, date added, and date modified.
- Change SIM activation state.
  - Select from: Inventory, Activation Ready, Activated, Deactivated, and Retired.
- View SIM Usage
  - Shows: Cycle start date, billable and total data, billable and total SMS, billable and total voice.
  - The cycle start date can be set using a YYYY-MM-DD format.
- Send SMS to SIM
- Change rate plan

You can access the supported operations in the device drilldown of a Jasper connected device after the following configuration steps are completed.


### Configuration for Jasper

In order to connect your Jasper service to your {{site.data.keyword.iot_short_notm}} organization there are two stages of configuration that must first be done. First, your {{site.data.keyword.iot_short_notm}} must be connected to your Jasper service, then your {{site.data.keyword.iot_short_notm}} devices must be configured.


1. Enable the Jasper extension. To enable Jasper integration with your {{site.data.keyword.iot_short_notm}} organization, complete the following steps:
  1. From the {{site.data.keyword.iot_short_notm}} dashboard, select **Extensions**.
  2. In the **Extensions** page, click **Add Extension**.
  3. Click **Add** next to Jasper.
  4. Enter your Jasper username, password, access key and domain ID.
  5. Click **Done**.

2. Configure your devices
You can configure the devices that are connected to both your {{site.data.keyword.iot_short_notm}} organization and your Jasper account to display data from Jasper in the {{site.data.keyword.iot_short_notm}} dashboard.  
**Important:** The Jasper configuration cannot be applied as part of the Add Device process, only previously connected devices can be configured with Jasper.  
To configure your Jasper-connected devices, complete the following steps:
 1. In the devices tab of your {{site.data.keyword.iot_short_notm}} dashboard, find the Jasper-connected device to be configured.
 2. Select the device to open the *Device Drilldown* view.
 3. Scroll down to *Extension Configuration*.
 4. Enter the extension configuration by using the following JSON format, and then click **Confirm changes** to save your configuration.  

```json  
    {
        "jasper": {
            "iccid": "string"
        }
    }

```

When the organization is successfully configured, the *Extensions* section displays under the *Extensions Configuration* section in the *Device Drilldown* view.

## AT&T
{: #att}

### Supported operations for AT&T

The AT&T extension enables the following AT&T operations:

- View overall AT&T data
  - Shows: Status, Rate Plan, month-to-date data usage, month-to-date SMS usage, month-to-date voice usage, overage limits, date added, and date modified.
- Change SIM activation state.
  - Select from: Inventory, Activation Ready, Activated, Deactivated, and Retired.
- View SIM Usage
  - Shows: Cycle start date, billable and total data, billable and total SMS, billable and total voice.
  - The cycle start date can be set using a YYYY-MM-DD format.
- Send SMS to SIM
- Change rate plan

### Configuration for AT&T

In order to connect your {{site.data.keyword.iot_short_notm}} organization to AT&T you must complete organization configuration and device configuration.

To configure your {{site.data.keyword.iot_short_notm}} platform, complete the following steps.

1. Enable the AT&T extension. To enable AT&T integration with your {{site.data.keyword.iot_short_notm}} organization, complete the following steps:
  1. From the {{site.data.keyword.iot_short_notm}} dashboard, select **Extensions**.
  2. In the **Extensions** page, click **Add Extension**.
  3. Click **Add** next to AT&T.
  4. Enter your AT&T username, password, access key and domain ID.
  5. Click **Done**.

In order to connect your {{site.data.keyword.iot_short_notm}} organization with your AT&T account, there are two stages of configuration that must first be done. Complete the the organization configuration and then configure your devices.


2. Configure your devices
You can configure the devices that are connected to both your {{site.data.keyword.iot_short_notm}} organization and your AT&T account to display data from AT&T in the {{site.data.keyword.iot_short_notm}} dashboard.  
**Important:** The AT&T configuration cannot be applied as part of the Add Device process, only previously connected devices can be configured with AT&T.  
To configure your AT&T-connected devices, complete the following steps:
 1. In the devices tab of your {{site.data.keyword.iot_short_notm}} dashboard, find the AT&T-connected device to be configured.
 2. Select the device to open the *Device Drilldown* view.
 3. Scroll down to *Extension Configuration*.
 4. Enter the extension configuration by using the following JSON format, and then click **Confirm changes** to save your configuration.  

```json  
    {
        "atnt": {
            "iccid": "string"
        }
    }

```

When the organization is successfully configured, the *Extensions* section displays under the *Extensions Configuration* section in the *Device Drilldown* view.

<!--
## ARM mbed connector
{: #arm}

The ARM mbed connector allows you to connect your ARM mbed device to your {{site.data.keyword.iot_short_notm}}. The ARM mbed extension is allows the ARM mbed portal and the {{site.data.keyword.iot_short_notm}} to send and receive data from the ARM mbed portal.

### Setup Configuration


1. Enable the ARM mbed connector extension. To enable the ARM mbed connector extension complete the following steps:
  1. From the {{site.data.keyword.iot_short_notm}} dashboard, select **Settings** and navigate to **Extensions**.
  2. In the **Extensions** menu, click **Add Extension**.
  3. Click **Add** next to ARM mbed connector extension.
  4. Enter your ARM mbed access key and domain ID. You can find these by using the ARM mbed portal at https://connector.mbed.com.
  5. Check the credentials are correct by clicking the **Check Connection** button.
  6. Click **Done**.

### Payload Format

There are two types of incoming messages from the ARM mbed platform, notifications and asynchronous responses. The {{site.data.keyword.iot_short_notm}} can send commands to devices that are connected to the ARM mbed platform.

#### Notifications

Notifications are generated by changes in device or sensor data. After the {{site.data.keyword.iot_short_notm}} processes the message, it is to the device event topic in the same way as a device connected directly to the {{site.data.keyword.iot_short_notm}}. The event type used for notifications originating on devices connected to the ARM mbed platform is `notify`.

The following code sample shows the payload format for a notification sent by the ARM mbed platform API:

```
{
  "ep":<endpoint/deviceID>,
  "path":<resource path>,
  "ct":<content type>,
  "payload":<Base64 encoded payload>,
  "max-age":<how long the payload is valid, in seconds>
}
```

#### Asynchronous responses

When the {{site.data.keyword.iot_short_notm}} sends a command to a device connected to the ARM mbed platform, the device sends a confirmation message back to the {{site.data.keyword.iot_short_notm}}. This confirmation message is called an _asynchronous response_ and uses the event type `asyncResponse`.

The following code sample shows the payload format for an asynchronous response sent by the ARM mbed cloud service:

```
{
  "id":<transaction id>,
  "status":<200 is command was sucessfully executed. Check other HTTP response codes>,
  "ct":<content type>,
  "max-age":<how long the payload is valid, in seconds>,
  "payload":<base64 encoded payload>,
  "ep":<endpoint/deviceID affected by the command>,
  "path":<resource path affected by the command>
}
```

#### Sending commands to the ARM mbed platform

The {{site.data.keyword.iot_short_notm}} can send commands to devices connected to the ARM mbed platform. Commands sent to the ARM mbed platform must use the following JSON format.

```
{
  "method":<PUT or POST>,
  "deviceId":<endpoint/deviceId>,
  "resourceId":<resource path>,
  "payload": <Base64 encoded payload>
}
```
The method chosen is case sensitive. The initial '/' of the resource path must be skipped.


The payload should be published to the following topic:

```
iot-2/type/<device_type>/id/<deviceId>/cmd/<command_type>/fmt/<command_format>
```
-->

## Orange
{: #orange}

The Orange extension allows you to view SIM card data from devices which are connected to your {{site.data.keyword.iot_short_notm}} and have an Orange SIM card installed.

https://developer.ibm.com/iotplatform/2016/03/30/watson-iot-platform-integration-with-orange-beta/

### Supported operations for Orange

If you have a device which is connected to your {{site.data.keyword.iot_short_notm}} service and has an Orange SIM card, you can use the Orange extension to view the following SIM card data:

- SIM serial number
- Activation status
- Last status change
- Last status refresh
- Location status

### Configuration for Orange



To enable the Orange extension:

1. From the {{site.data.keyword.iot_short_notm}} dashboard, select **Extensions**.
2. In the **Extensions** page, click **Add Extension**.
3. Click **Add** next to the Orange extension.
4. Enter your Orange user name and password.
6. Click **Done**.

After the Orange extension has been enabled, each device with an Orange SIM card must be configured to display Orange SIM data.

1. In the devices tab of your {{site.data.keyword.iot_short_notm}} dashboard, find the Orange SIM device to be configured.
2. Select the device and scroll down to *Extension Configuration*.
3. Enter the extension configuration by using the following JSON format, and then click **Confirm changes** to save your configuration.

```  
    {
        "orange": {
            "serialnumber": "<serial number of Orange SIM>"
        }
    }

```
When the organization is successfully configured, the *Extensions* section displays under the *Extensions Configuration* section in the *Device Drilldown* view.

## Historical Data Storage
{: #historical_data}

The historical data storage extension lets you locate and configure compatible message storage services such as [{{site.data.keyword.cloudantfull}}](../../cloudant_connector.html) or [{{site.data.keyword.messagehub_full}}](../../message_hub.html) for your IoT data.

## Custom Device Management Packages
{: #device_mgmt}

Device management is a core feature of the {{site.data.keyword.iot_short_notm}}, however, it can be extended to develop additional functionality.

The device management extension allows you to install custom functions for device management. For more information on custom device management functions, see [device management custom extensions](../../devices/device_mgmt/custom_actions.html){: new_window}.


## The Weather Company
{: #weathercompany}

The Weather Company extension combines weather data with your existing {{site.data.keyword.iot_short_notm}} devices. Weather data from The Weather Company appears in the device details view if an update location request has been made by using the API, or if the device has already set its location by using a device management message.

**Note:** Only managed devices can set their own locations. All unmanaged devices must have their locations set manually by using the API. For more information on setting a device location, see [Update Location requests](../../devices/device_mgmt/index.html#update-location).

<!--
### Weather Data

To view the weather data retrieved for a device location, find the device in the **Devices** pane and click on it. In the detailed device view scroll down to the **Extensions** section. The following weather data is listed:

- Current weather.
- Current temperature.
- Predicted maximum and minimum temperature.
- Relative humidity.
- Pressure.
- Visibility.
- Wind speed.
- Wind direction.
- Latitude.
- Longitude.

Weather data from The Weather Company extension can be retrieved by using the API. For information on the Weather Company API, see [The Weather Company API documentation](https://docs.internetofthings.ibmcloud.com/swagger/ext-twc.html).
-->
