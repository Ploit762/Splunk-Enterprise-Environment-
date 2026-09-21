# Splunk Universal Forwarder Install

The Splunk Universal Forwarder allows you to forward data like stream log data, into a central Splunk environment. It gathers logs, files, Windows Event logs, firewalls and servers if you have one. You can use the other option which is "Monitor", but this will only pull local files systems directly from your device that Splunk is installed on, and not the other devices that is on the network.
#
* To access the Universal Forwarder, go to https://www.splunk.com/en_us/download/universal-forwarder.html</a>. Make sure that you have a Splunk account with a active email.
* Once you are on the "Start your free trial" page, sign into your account. From there you can scroll down the page until you see the Operating system that you are wanting to install Splunk on. I will be using "Windows 10,11 Windows Server.msi".
* Make sure to let the installed download full, and then run the install in admin mode.
#

* When you first enter the installer, you will be prompted with a screen that ask about license agreement. make sure to check the box that states "Check this box to accept the License Agreement". After that, you can click the "Customize Options" button. You can leave everything else as it is.
  * <img width="450" height="400" alt="Screenshot 2026-09-20 185314" src="https://github.com/user-attachments/assets/01acb8a0-0d31-457a-a4cc-40e80bffa74f" />

* Verify that your directory is what you want to be, then click "Next". You can ignore and click "Next" on the SSL certificate prompt as you will not be needing it if you are just doing this on your own device.
* Click on "Virtual Account" on the next prompt, then click "Next".
* On the next prompt, you can select different things you would want Splunk to monitor and log log to you. I selected all that was there, feel free to choose what you are wanting to see within your Splunk Enterprise, then click "Next".
  * <img width="450" height="400" alt="Screenshot 2026-09-20 185654" src="https://github.com/user-attachments/assets/1cf260c7-b6ba-49bb-a3bf-76c42ca1b6d9" />

* On the next prompt, put in credentials for a admin account. Remember this account because this is the account that you will be signing into Splunk Enterprise with, click "Next" after you are done.
* For the next prompt, put your Hostname or IP address and use the default port that is given to you by Splunk. You can find your IP address or Hostname in the search box within your Splunk Enterprise. it will be everything before the `8000` within the search box above. Make sure to take out the forward slashes and the `http:`. After you click "Next", do the same thing for the next prompt, but default port will be `9997`.
* After you click "Next", click "Install". Wait for the Splunk to fully download. After the install is done, click "Finish".
* Go to your Splunk Enterprise, click "Search & Reporting", and then click on "Data Summary".
* If you set everything up correctly, you would be able to see your host name of your device along with the "Count" and "Last Update" columns.
* For your first SPL search, you can confirm everything is coming through by searching `host="your host name"`. This is going to show you data that is associated with that host name.
*  Make sure to set the "Time range" to "All time", and change the mode to "Verbose Mode" so you can view all events & field data. Press enter in the search box after everything as been selected.
#
From here you are look into your "Indexes" and look at different events that had occurred within your network.

