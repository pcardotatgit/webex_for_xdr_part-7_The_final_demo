# Webex for XDR demo part 7 - the final demo

This article is the last one of the serie dedicated to use Webex as an alerting system for Cisco XDR.

We put everything together and show the final result.

## Step by Step demo installation

### Step 0 : pre requisits

-	If not already done create an XDR API client ( client-ID and client password ) into your XDR tenant
-	Create a webex bot and copy it’s authentication token
-	From your webex client start a Webex conversation with the Webex Bot

### Step 1 Create XDR Feeds 

[Create Text Public Feeds for firewalls](https://github.com/pcardotatgit/SecureX_Workflows_and_Stuffs/tree/master/12-create_securex_blocking_lists_for_firewalls)

### Step 2 Fill the XDR IP V4 feed with TOR network IP addresses :
[TOR BLOCKING LIST TO IPV4 SECUREX FEEDS](https://github.com/pcardotatgit/SecureX_Workflows_and_Stuffs/tree/master/500-SecureX_Workflow_examples/Workflows/TOR_IP_blocking_list_to_SecureX_feeds)

### Step 3 configure the XDR IPV4 feed URL into the SCA Third Party Watch List

Into your SCA ( XDR Analytics ) tenant, create a new third party watchlist based on the XDR IPv4 feed created above.

For doing so, go to Settings => Alerts => Third Party Watch List and create a new feed . Click on the [ Add External URL ] and use the public URL you got into XDR when you created the IPv4 Feed.

### Step 4 setup the Webex Alerting system

Deploy into your XDR tenant the [XDR_ALERT_CARD_WITH_TARGETS_AND_OBSERVABLES_TO_WEBEX_ROOM](https://github.com/pcardotatgit/webex_for_xdr_part-6_XDR_send_alert_workflow) Incident workflow

### Step 5 Install the XDR lab_simulator-002

[lab_simulator-002](https://github.com/pcardotatgit/lab_simulator-002)

**You are ready to go !**

## The demo flow
