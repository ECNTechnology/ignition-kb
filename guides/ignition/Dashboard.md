---
title: Dashboard
date: 2021-12-22T06:25:00.676Z
---
# myCloudPBX Dashboard

## What's on your myCloudPBX Dashboard?

The Dashboard displays critical information about your myCloudPBX system, providing granular reporting data for a real-time or historical view of the activities within your phone system. 

Drill down into user performance and call reports for valuable insight into resolution times, response rates and optimal service times.

## Feedback

**Are there any reports or charts you would like to see?**

Let us know!

Simply click the feedback bubble and send us your valued feedback. This will assist us in making improvements to the Dashboard and reporting.

![](../../images/feedback.gif)

## Dashboard Widgets

The Dashboard drills down into user performance and call reports, giving valuable insight into resolution times, response rates and optimal service times.

![](../../images/dashboard_widgets.png)

### Create a new Dashboard

From the left hand menu, click the <img style="width: 25px; height: auto;" src="../../images/dashboard_homeicon.png"> '**Home**' button.

![](../../images/dashboard_actionaddbutton.png)

On the top right hand corner click the '**Action**' button, then click '**Add**'.

![](../../images/widgets_addnew.png)

Select '**Blank Dashboard**'.

![](../../images/dashboard_addnew.png)

Name your new Dashboard and click the <img style="width: 50px; height: auto;" src="../../images/dashboard_submitbutton.png"> button.

### Adding Widgets

To add widgets to the Dashboard, click the <img style="width: 50px; height: auto;" src="../../images/dashboard_plusbutton.png"> button.

![](../../images/dashboard_widgetlist.png)

When you select a widget, you may be asked to choose some additional settings. Do so, then click the <img style="width: 50px; height: auto;" src="../../images/dashboard_submitbutton.png"> button.

### Unique URL for Wallboards

You can also generate a unique URL for each specific Dashboard, allowing you to keep a close eye on your statistics.

![](../../images/dashboard_uniqueurl.png)

On the top right hand corner click the '**Action**' button, then click '**unique URL**'.

Copy the URL that is provided and open it on any web browser.

## Real Time Status Widget Page

The '*Real Time Status*' widget allows you to keep a close eye on your call queues.

## Adding the 'Real Time Status' Dashboard

From the left hand menu, click the <img style="width: 25px; height: auto;" src="../../images/dashboard_homeicon.png"> '**Home**' button.

![](../../images/dashboard_actionaddbutton.png)

On the top right hand corner click the '**Action**' button, then click '**Add**'.

![](../../images/widgets_addnew.png)

Select '**Real Time Status**'.

![](../../images/widgets_realtimeadd.png)

* Select the PBX from the dropdown list and click the <img style="width: 50px; height: auto;" src="../../images/dashboard_submitbutton.png"> button.
* Add a description. This will show as the name of the tab.

### Navigation

![](../../images/queues_leftmenu.png)

If you have more than one call queue running you can choose between them from the left hand menu.

::: tip
**Note:** You can also see the 'queue type' listed here.
:::

### Statistics

![](../../images/queues_topmenu.png)

Here you can see the following information:

* **Total Calls:** Total number of calls entering this queue today.
* **Abandoned Calls:** Number of calls that entered the queue today that hung up and were not answered. All abandoned calls shown here will also be visible on the abandoned call report available <a href="https://kb.mycloudpbx.com.au/guides/mycloudpbx/dashboard.html#abandoned-calls">here</a>.

  ::: tip
  **TIP:** Click the button for 'Abandoned' to see a list of abandoned calls for today.
  :::
* **Timed Out / Exits:** Number of calls that entered the queue today, were not answered and progressed to the next activity. If the caller uses the 'press 1 to leave a voicemail' option, this will count towards the 'timed out/ exits' tally.

  :::tip

  **Note:** A call that times out, is not classified as abandoned.

  :::
* **Avg. Wait Time:** Average time callers waited prior to being answered.
* **Avg. Talk Time:** Average time spent talking on calls answered in this queue.

### Agent Status Information

![](../../images/queues_agentstatus.png)

Here you can see the following information:

* **Name:** Displays the name of the agent.
* **Extension:** Displays the extension number of the Agent.
* **Talking to:** Displays the caller ID (where available) of the person the agent is speaking with.
* **Time In Call:** Displays the total time the agent has been on their current call.
* **Call Status:** Will show as either '**Available**' or '**In Call**'

### Calls In Queue Information

![](../../images/queues_inqueue.png)

Here you can see the following information: 

* **Start Time:** This is the time the caller entered this call queue.
* **Caller ID:** Displays the caller ID (where available) of the person waiting in the queue.
* **Waiting Time:** Displays the total time each caller has been waiting (in the current queue). 

:::tip 
**Note:** Each call queue will have it's own '**Waiting time**'.
:::

## Call Reports

### Inbound Calls

The '**Inbound Calls**' report shows the total number of incoming calls answered by a user, filtered by the phone number & time period selected.


* Select any time period with a maximum of 7 days between them.
* Choose any phone number, or all phone numbers.

Click <img style="width: 100px; height: auto;" src="../../images/dashboard_inbound_calls_csv.png"> to download a copy in CSV format.

![](../../images/dashboard_inbound_calls.png)

#### Inbound Calls CSV Headings

* **CallGuid:** Unique reference for the call.
* **CallDateTime:** Date/Time the call took place.
* **Duration:** Duration of the call.
* **OriginNumber:** The originating caller ID.
* **TargetNumber:** The destination number on the PBX.
* **CallRouteName:** Reserved for future use.
* **TalkerCount:** Every time the call is transferred to another user on the PBX this will increment. An answered call will show at least 1 Talker.
* **TalkerTime:** Total time of the call once answered.
* **TimeToAnswer:** Time taken before the call was answered.
* **FirstExtension:** For answered calls, this shows the extension number that answered the call.

### Abandoned Calls

The '**Abandoned Calls**' report displays the total number of inbound calls where no user spoke to the caller and it did not go to Voicemail.
**Note:** Calls that go to Virtual Fax, or the conference bridge should not appear in this report.

* Select any time period with a maximum of 7 days between them.
* Tick the checkbox if you wish to include calls that went to voicemail.

Click <img style="width: 100px; height: auto;" src="../../images/dashboard_inbound_calls_csv.png"> to download a copy in CSV format.

![](../../images/dashboard_abandoned_calls.png)

### Outbound Calls

The '**Outbound Calls**' report displays the total number of outgoing calls - categorised into Local, National, Mobile, International, and 13/Misc calls. 

Report results can be filtered by simply clicking on the Call Type labels in the legend.

* Select any time period with a maximum of 7 days between them.
* Report can be filtered by clicking on the labels in the legend on the right hand side.
* Hover over the bar graph to see the exact number of calls.

Click <img style="width: 100px; height: auto;" src="../../images/dashboard_inbound_calls_csv.png"> to download a copy in CSV format.

![](../../images/dashboard_outbound_calls.png)

### Time to Answer

The '**Time to Answer**' report displays the average time taken for a call to be answered by a user.

* Select any time period with a maximum of 7 days between them.
* Choose a phone number / numbers from the drop down menu.

Click <img style="width: 100px; height: auto;" src="../../images/dashboard_inbound_calls_csv.png"> to download a copy in CSV format.

### Export Call Records

#### Background information about the 'Export Call Records' report.

The '**Export Call Records**' report allows you to download an easy to digest csv report with the following headings:

* **Callguid:** Unique Identifier of the Call.
* **Calldatetime:** Date / Time of the Call.
* **Serviceid:** Unique Identifier of the Service that made/received the call.
* **Servicename:** myCloudPBX Service Name generated when the PBX was first created.
* **Servicefriendlyname:** Customer defined Service Name.
* **Direction:** Call Direction , In for Inbound calls, Out for Outbound Calls, Int for Internal calls.
* **Dialplan:** Dialplan Used: AU (Australia), NZ (New Zealand)
* **Originnumber:** The Callers Number.
* **Targetnumber:** The Called Number.
* **Jurisdiction:** The 'International Jurisdiction' (Used for International billing).
* **Jurisdictiondesc:** Internal Call Jurisdiction Name.
* **Duration:** Total Duration of the Call in Seconds.
* **Billabletime:** (Outbound calls only) - Billable time in seconds.
* **TimeToAnswer:** 

  * Ringtime for outbound call. 
  * For inbound calls this is the time to answer for the first talker (in seconds).
* **Ratetype:** Outbound Calls only. The Rate Type of the call.

  * 1. Local
  * 2. National
  * 3. International
  * 4. Mobile
  * 5. Calls to 13/Misc
  * 7. Calls to 1800
* **Hangupreason:** The hangup reason for the call.
* **Originuseragent:** Where available, this will show the user agent that made the call.

  * Outbound: The Identifier of the device that made the call.
  * Inbound: The Identifier of the device that received the call.
* **Accountcode:** Used with 'Account Code Dialling', will show the account code that was dialled.
* **Rtpmos:** IP telephony call quality rating - MOS - Mean Opinion Score, rating of 1 through 5 (5 being the best).

  * When using the G711 codec, this can be as high as 4.5.
  * When using the G729 codec, this can be as high as 3.9.
* **Rtpquality:** IP telephone call quality percentage rating - 1 through 100 (%)
* **ExtensionNumber:** 

  * Outbound: The extension number of the extension making the call.
  * Inbound: The extension number of the first talker.
* **ExtensionName:** Then extension name for the ExtensionNumber.
* **OfficeName:** For outbound calls, this will show which "*Office*" the extension who originated the call belongs.
* **IPOwner:** The details of the IPAddress Holder (Service Provider).
* **IPAddress:** The IP Address of the UserAgent.

#### Usage

Select the start and end date ranges as well as the phone number(s).

![](../../images/export_call_records_1.png)

Click <img style="width: 100px; height: auto;" src="../../images/dashboard_inbound_calls_csv.png"> to download a copy in CSV format.

You can also schedule this report by clicking the  <img style="width: 150px; height: auto;" src="../../images/scheduled_button.png"> button.

### Cost Allocation

#### Background information about Account Codes

Account codes are used to attribute calls to either a user or group of users.  Alternatively, account codes can be used to attribute calls made to your customers. 

When a call is made, you can enter the account code as part of the phone number.  The code will show up in the CDR (Call Detail Recording) with call length, number dialled etc.  The CDR record is written when you terminate the call.

This functionality would typically be used by anyone who bills specifically for their time, eg: lawyers.

#### Usage

The '**Account Code**' report takes each call with account codes  and assigns them a dollar value.

* Specify the start & end date ranges.
* Assign the following values to each of the call types:

  * **Unit:** Choose from 1 second, 30 seconds, or 1 minute increments.
  * **Cost:** Enter the cost (per unit) in cents.
  * **Minimum:** Enter the minimum call cost, in cents.
  * **Flagfall:** Enter the flagfall rate here. (This is the cost that is applied once the call is connected.

Click <img style="width: 100px; height: auto;" src="../../images/dashboard_savebutton.png"> to save your settings.

* Choose from Excel or PDF format, then download either the '**Summary**' or '**Detailed**' report.

![](../../images/dashboard_account_code.png)

### Call Recordings

The '**Call Recordings**' page allows you to play or download recorded calls. Calls can be searched by the calling number (origin), or the called number (target).

* Select the start & end dates.
* Enter a number to search (if required)

Click <img style="width: 50px; height: auto;" src="../../images/dashboard_callrecordings_getcalls.png"> 

Once the data has loaded, you will be able to see the following information about each call:

* **Origin:** This is the source number.
* **Target:** This is the destination number.
* **Duration (sec):** Duration of the call, measured in seconds.
* **Call Date:** Date / Timestamp of the call.
* **Download:** Click here to download a copy of the call recording.
* **Play:** Click here to play the recording.

![](../../images/dashboard_callrecordings.png)

## User Reports

### Active Users

The '**Active Users**' report shows the total time users spent on calls.  Reports are filtered by the direction of the call, the office, and time period selected.

* Select any time period with a maximum of 7 days between them.
* Select your '**Call Direction**':

  * All
  * Internal (This will only display calls made internally.
  * Inbound (This will only display ***inbound calls***. (calls that you answered).
  * Outbound (This will only display ***outbound calls*** (calls that you made).  
  * Select the '**office**', or simply select '*all offices*'.

**Group by:**
You can choose to group by extension number, or by the users' name by using the <img style="width: auto; height: 25px;" src="../../images/slider.png"> slider.


::: tip

 **TIP:** You can also choose between a **bar graph** and a **pie chart** by clicking the button in the top right hand corner of the graph.

:::

![](../../images/active_users_top.png)

![](../../images/active_users_bottom.png)


![](../../images/dashboard_active_users_pie.png)

### Total Call Count

The '**Total Call Count**' report shows the total number of calls each user made or received, filtered by the office and time period selected.

* Select any time period with a maximum of 7 days between them.
* Select your '**Call Direction**':

  * All
  * Internal (This will only display calls made internally.
  * Inbound (This will only display ***inbound calls***. (calls that you answered).
  * Outbound (This will only display ***outbound calls*** (calls that you made).  
* Select the '**office**', or simply select '*all offices*'.

**Group by:**
You can choose to group by extension number, or by the users' name by using the <img style="width: auto; height: 25px;" src="../../images/slider.png"> slider.




![](../../images/total_call_count_top.png)

![](../../images/total_call_count_bottom.png)

### Average Call Duration

The '**Average Call Duration**' report displays the average time each user spent on a call. Reports are filtered by the direction of the call, the office, and the time period selected.

* Select any time period with a maximum of 7 days between them.
* Select your '**Call Direction**':

  * All
  * Internal (This will only display calls made internally.
  * Inbound (This will only display ***inbound calls***. (calls that you answered).
  * Outbound (This will only display ***outbound calls*** (calls that you made).  
* Select the '**office**', or simply select '*all offices*'.

::: tip

 **TIP:** You can also choose between a **bar graph** and a **pie chart** by clicking the button in the top right hand corner of the graph.

:::

**Group by:**
You can choose to group by extension number, or by the users' name by using the <img style="width: auto; height: 25px;" src="../../images/slider.png"> slider.


![](../../images/average_call_duration_top.png)

![](../../images/average_call_duration_bottom.png)

## Scheduled Reporting

Scheduled Reporting allows you to create a report and receive it in your inbox when you need it.

If a report is available for scheduling, you will see this button: <img style="width: 150px; height: auto;" src="../../images/scheduled_button.png">

### Creating a report

Click the <img style="width: 150px; height: auto;" src="../../images/scheduled_button.png"> button to create your report.

<img style="width: 1000px; height: auto;" src="../../images/scheduled_create_new.png">

* **Report:** This is the report type.
* **Friendly Name:** This is your name for the report.
* **Email:** Add as many email recipients as required.
* **Schedule:** Choose from Daily, Weekly, or Monthly.

  * **Daily:** Select the days you wish to receive the report.
  * **Weekly:** Choose the day of the week you wish to receive the report.
  * **Monthly:** Choose the day of the month you wish to receive the report.
* **Report State:** Use the toggle switch to choose from ON or OFF.
* **Period:** Choose from the last 7 days, 14 days, or the last month.
* **Direction:** Choose from Inbound, Outbound, Internal, or All Calls.
* **Offices:** Choose from a specific office, or all offices.

When you are finished, click the <img style="width: 50px; height: auto;" src="../../images/scheduled_save.png"> button.

### View / Modify Existing Reports

Click **Scheduled Reports** from the left hand menu.

Here you can see the reports scheduled for the PBX including the report type, schedule, operating status, and the date last run.

<img style="width: 1000px; height: auto;" src="../../images/scheduled_viewlist.png">

* To edit a report, click <img style="width: 50px; height: auto;" src="../../images/scheduled_edit.png">.
* Use the toggle switches to enable or disable a report.
* To delete a report, click <img style="width: 50px; height: auto;" src="../../images/scheduled_delete.png">.

## Virtual Fax Archive

The '**Virtual Fax Archive**' allows you to download your inbound Fax.

Click the '**Download**' button to download a copy of the PDF.

![](../../images/dashboard_vfax.png)

::: tip

 **NOTE:** Fax are stored for 90 days only

:::