## FTS Infrastructure
![image](https://user-images.githubusercontent.com/60719165/183449678-e2c153e3-0eea-4cd9-bc69-63b4adb10491.png)

TAK Infrastructure thoughts: Give some thought to how you are going to deploy FTS server.
 1. **Cloud** - A Digital Ocean (DO) or other virtually hosted server will allow quickest deployment and is scalable to as many users as you wish
 2. **LAN** - An RPi server located on your home/office LAN may require additional complexities for non-LAN TAK clients to access your server, e.g. dynamic
DNS services (noip.com) and NAT port forwarding.
 3. **VPN** - An RPi server running as a ZeroTier (or other SD-WAN) client will mostly circumvent the need for the complexities listed above and allow any TAK
client on the ZeroTier network to access the RPi server regardless of internet connection method (broadband, cellular data, etc.)
 4. **Edge** - An RPi server running on an ad hoc or local infrastructure LAN configuration – Can be setup completely off-grid and without reliance on a
functioning internet, but will suffer significant limitations in range for TAK clients to connect.
 5. **Hybrid off-grid** – A DO installed server or RPi with one or more of the TAK clients connected as a “bridge” to an off-grid mesh network such as Meshtastic
LoRa. This configuration will allow any off-grid Meshtastic clients to have their communications reach all “internet-connected” TAK clients via a
TAK client who is simultaneously connected to both the internet and mesh sides of the network.