# NetworkManager

This component can be used to provide information about network. The blocks for this component are as follows:

**IsConnected: **Use this block to determine if device has network connectivity. Will return true if connection is through WiFi or Mobile Network

![](/assets/networkMgr1.png)

**IsGPSEnabled**: Use this block to determine if GPS is enabled

![](/assets/networkMgr3.png)

**StartGPSOptions**: If device isn't connected to GPS, you can start this block to startup the GPS options

![](/assets/networkMgr2.png)

**GetConnectionType**: Use this block to determine the connection type; e.g. WiFi or Mobile

![](/assets/networkMgr4.png)

**IsFastConnection**: Use this block to determine if device has slow or fast connection. Useful when there is a need to download large files

![](/assets/networkMgr6.png)

