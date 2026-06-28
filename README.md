# Splunk Enterprise Install

Splunk is a platform that acts as a universal search engine for your network infrastructure weather at home or in a business. It analyzes data in real time and acts as the central brain to for all sources within your network and monitors it.
#
You first want to create a account at https://www.splunk.com/</a>. After this is done you then want to go click on `Trials & Downloads`. After you click on that, you then want scroll down to "Splunk Enterprise" and click `Log in to your Spluunk account to download`. After you log in, click on the operating system you currently have, choose the file you are wanting to download, and click the download button. Usally the download will start automatically, but if it doesn't, click the `Try this URL`.

* Once this has finished downloading. Check the box that says `Check this box to accept the License Agreement`.
* Put in a username and password of your choice and click "Next" and then "Install"

  *<p align="center">Let the install run all the way through, it may take a while.</p>*

  * After the install is down click "Finish" to launch a browser with Splunk.
  * Once this is finished, you will then want to check "Services" in Windows and see if Splunk is running. This will be under `Splunkd`, or `splunkd Service`. If this is runnging, then Splunk has been installed correclty.
#
Once Splunk has been installed one thing you want configure is `port forwarding` and `Receive data`. This can be done by going to `Forwarding and receiving`, "Add New" Configure receiving, and then to receive data on the default TCP port for Splunk, type "9997". 
#
Putting in the port for data receiving and forwarding is only enabling the port, but no traffic will come through yet. You can download "Splunk Universal Forwarder" here https://www.splunk.com/en_us/download/universal-forwarder.html</a>. This wil allow you to forward data from your computer to the Splunk server. 
*<p align="center">I will go over how to set up the "Splunk Universal Forwarder" in another file within this repositories. </p>*
