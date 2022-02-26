---
title: PBX Configuration
date: 2021-12-15T10:41:12.066Z
---
# **PBX Configuration**

- - -

## Blocklist Numbers
In the event you wish to block a number from calling you, add it to the myCloudPBX Blocklist.

From the PBX Configuration page, click ‘**Blocklist**’.  <img src="../../images/blocklist.png" alt="blocklist icon" title="blocklist icon" height="50px"/>

<img src="../../images/mycloudpbx_blocklist.png" alt="blocklist" title="blocklist"/>



Click '**Add Blocked Callers**’.

Add the phone number, and click '**Save**'.

You will never receive a call from this number again.

**Note:** This will only work if the caller ID is public. 

## Call Diversions

Call diversions can be enabled in a number of ways, the easiest of which is to enable '**Call Forward All**' on the inbound route.

Select ‘**Call Routing**’ from the PBX homepage.

<img src="../../images/call_routing.png" alt="call routing" title="call routing"/>


Find the number for which you wish to enable call forwarding on and then click '**view/edit**'.

<img src="../../images/call_routing_forward.png" alt="call routing forwarding options" title="call routing forwarding options"/>

 
Scroll down until you see the '**Enable Forward All**' option.

Make sure that it is ticked and note down the '**Allocated Dial Code**'

**To Enable Call Forwarding**: Dial the allocated dial code, followed by the destination.

**To Disable Call Forwarding**: Dial the allocated dial code, and after the tone, hangup.


<div class="custom-block tip"><p class="custom-block-title">Note</p> <p> The Allocated Dial Code is unique for each call route.</p></div>

## Call Recordings

Call recordings can be enabled for inbound calls (per call route), outbound calls (per extensions), or both.

### Enable Call Recording Application

To turn on call recordings for a call route, you must first enable the call recording functionality on your PBX.
From the PBX Configuration screen, click ‘**Manage Applications**’. <img src="../../images/applications_icon.png" alt="applications icon" title="applications icon" height="50px"/>

<img src="../../images/ignition_callrecording.png" alt="enable call recording" title="enable call recording"/>

Scroll down until you see '**Call Recording**'.

Tick ‘**Call Recording**' on.

You will now need to go back to the PBX Configuration page to enable recordings for either inbound calls, outbound calls, or both as per your needs.

### Inbound Calls

To enable call recordings for an inbound route, select '**Call Routing**' from the PBX homepage.

<img src="../../images/call_routing.png" alt="enable call recording for inbound calls" title="enable call recording for inbound calls"/>

Find the number for which you wish to enable call recordings and then click '**view/edit**'.

<img src="../../images/call_routing_recording.png" alt="enable call recording for inbound calls" title="enable call recording for inbound calls"/>

Click the checkbox to '**Enable Call Recording**' for all inbound calls.

Scroll down to the bottom of the page and click '**Save**' to save your changes.

Your changes are now ready to be applied to the PBX.

<img src="../../images/apply_changes.png" alt="pending changes" title="pending changes"/>

Click ‘**Apply Changes**’.


<img src="../../images/ignition_apply_changes_scheduled.png" alt="applied changes" title="applied changes"/>

### Outbound Calls

To enable call recordings for outbound calls, select '**Offices & Users**'  from the PBX Configuration screen. <img src="../../images/icon_officesandusers.png" alt="offices & users icon" title="offices & users icon" height="50px"/>

<img src="../../images/ignition_offices_and_users.png" alt="offices and users screen" title="offices and users screen"/>

Select the extension you wish to modify.

Scroll down to ‘**Security & Other Features**’, then enable ‘**Record calls from this extension**’.

Click ‘**Save**’ when finished. 

Your changes are now ready to be applied to the PBX.

<img src="../../images/apply_changes.png" alt="pending changes" title="pending changes"/>

Click ‘**Apply Changes**’.


<img src="../../images/ignition_apply_changes_scheduled.png" alt="applied changes" title="applied changes"/>

### Shortcut Codes

During an active call you can use the following shortcut codes.

**Call Recordings must be enabled.**

-	If a recording is active **#8** will stop the current recording.

-	If a recording is not currently active **#8** will start an adhoc recording.

-	If a recording or adhoc recording is active **#7** will enabling masking of the recording.

-	If a call is currently masked **#7** will stop masking.

### Accessing Call Recordings

There are two ways to access your call recordings.

-	FTP

-	Hosted PBX Dashboard

### Call Recording Encryption

**Generating a Public/Private key pair.**

To enable call recording encryption you will first need to generate a Public/Private key pair.

To create a Public/Private key-pair we recommend using OpenSSL

#### Windows users

Download OpenSSL for Windows (https://wiki.openssl.org/index.php/Binaries (opens new window))

To run the commands below, go to the OpenSSL32 directory on your PC, and change to the /bin directory

**Note:** You may need to open the command prompt with admin privileges (run as administrator) and you will need to restart your computer before generating a certificate.

#### Mac users

OpenSSL comes shipped with Mac OS X version 10.6.2 onwards.

You can use Terminal to run OpenSSL (Open Applications > Utilities > Terminal or search for ‘**terminal**’ using the search bar in the top right hand corner of your screen) run the commands below.

**Note:** You may need to run each OpenSSL command lines with elevated privileges. – add _sudo_ before each command as needed.

#### Using OpenSSL

The basics command line steps to generate a private and public key using OpenSSL are as follows:

<div class="custom-block tip"><p class="custom-block-title">COMMAND</p> <p>openssl req -newkey rsa:2048 -nodes -keyout myprivatekey.pem -x509 -days 1825 -out mypublickey.pem</p></div>

<div class="custom-block warning"><p class="custom-block-title">WARNING!</p> <p>STORE YOUR PRIVATE KEY IN A SAFE, SECURE LOCATION. IF THE PRIVATE KEY IS LOST, ENCRYPTED FILES CAN NOT BE DECRYPTED</p></div>

#### Enabling Call Recording Encryption

To turn on call recordings for a call route, you must first enable the call recording functionality on your PBX.

From the PBX Configuration screen, click ‘**Manage Applications**’. <img src="../../images/applications_icon.png" alt="applications icon" title="applications icon" height="50px"/>


Enable the call recording encryption and paste a copy of your **PUBLIC KEY**. 
<div class="custom-block tip"><p class="custom-block-title"></p> <p>To learn how to generate a private key, click [here](https://kb.channelhaus.com.au/guides/ignition/pbx_configuration.html#call-recording-encryption)</p></div>


Click '**Save**'

Recorded calls will now have an “.enc” suffix to identify call recorded with a user provided public key.


#### Decrypting Call Recordings

To decrypt call recordings, use the following command. (Adjust for your filename..)

<div class="custom-block tip"><p class="custom-block-title">COMMAND</p> <p>openssl smime -decrypt -binary -in RECORDING_NAME.mp3.enc -inform DER -out RECORDING_NAME.mp3 -inkey myprivatekey.pem</p></div>


## Voicemail

### Personal Voicemail

Each extension has the option to have personal voicemail enabled. This voicemail will only plan if an extension is **directly dialled** (not part of a ring group).

#### Enable Voicemail on Extension

To configure voicemail on an extension, click on the '**Offices & Users**' icon from the PBX Configuration screen. <img src="../../images/icon_officesandusers.png" alt="offices & users icon" title="offices & users icon" height="50px"/>

<img src="../../images/office_and_users_list.png" alt="offices and users" title="offices and users"/>

Select the extension you wish to modify.

Scroll down until you reach the '**Voicemail**' section.

<img src="../../images/enable_voicemail.png" alt="enable voicemail" title="enable voicemail"/>

To enable the voicemail feature, tick '**Enable Voicemail**'

Here you can set the following information:

* **Voicemail PIN**: This is the PIN you will enter to access the voicemail system.
* **Send Messages to my Mailbox**: When selected, the voicemail will be emailed to the address nominated.
* **Delete messages after emailing them**: When selected emails will no longer be retrievable from your handset and will be only accessed via email.

Scroll down the page and click '**Save**' when you are finished.



<img style="width: auto; height: auto;" src="../../images/apply_changes.png">

Your changes are now ready to '***Apply***' to your PBX.

Click '***Apply Changes***'.

#### Accessing Voicemail

To access the Voicemail system, dial **777** from your phone, or press the '_**Voicemail**_' Button on your handset if it has one.

The voicemail system will then prompt you to enter your _**PIN**_ followed by the **\#** key.

Once authenticated to the voicemail system, you will be able to follow the prompts to record your personal voicemail messages, and listen to voicemails left for you.

