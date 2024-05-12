Objectives


Windows Defender Firewall is a host-based software firewall that is included with the Windows operating system.

learn to configure firewall rules using Windows Defender Firewall and Windows Defender Firewall with Advanced Security.

Configure Firewall Rules Using Windows Defender Firewall
Configure Firewall Rules Using Windows Defender Firewall with Advanced Security


Task 1: Configure Firewall Rules Using Windows Defender Firewall
In this exercise we will review Windows Defender Firewall configuration.

Click the Windows Start button. and then select Windows Security.
Windows Start menu with Windows Security selected

Click Firewall & network protection.
Security at a glance window with Firewall & network protection selected
Here you will see the firewall status for the following:
1
**Domain network:** Domain networks are workplace networks. A computer must be a part of the domain in order to communicate with other computers on that network. 
Copied!
1
**Private network:** Private networks are discoverable networks, meaning that only devices on that network can see or discover other devices on that same network. Home networks are a good example of a private network. 
Copied!
1
**Public network:** Public networks are non-discoverable networks. A non-discoverable network is a network where your device cannot be discovered by other devices on your network. A coffee shop or a library would be a good example of a public network. You do not want other individuals to be able to discover your device.
Copied!
Firewall & network protection window shows Domain network, Private network, and Public network status
Click Domain network.
Firewall & network protection window highlights Domain network
Verify that the Windows Defender Firewall is toggled to On.
Observe the option Incoming connections. If you need to block all incoming domain network traffic, including traffic that is typically allowed, then you only need to activate this option. You do not need to enable this option for this lab.

Note that if you have installed a 3rd Party anti-virus software, this option will be disabled. In this case, you can control the firewall settings only through the anti-virus software.

Select the back arrow button to return to the Firewall and network protection window.

Domain network details
Click Private network.
Firewall & network protection window highlights Private network
Verify that the Windows Defender Firewall is toggled to On.
Observe the option Incoming connections. If you need to block all incoming domain network traffic, including traffic that is typically allowed, then you only need to activate this option. You do not need to enable this option for this lab.

Note that if you have installed a 3rd Party anti-virus software, this option will be disabled. In this case, you can control the firewall settings only through the anti-virus software.

Select the back arrow button to return to the Firewall and network protection window.

Private network details
Click Public network.
Public network highlighted on Firewall & network protection window
Verify that the Windows Defender Firewall is toggled to On.
Observe the option Incoming connections. If you need to block all incoming domain network traffic, including traffic that is typically allowed, then you only need to activate this option.You do not need to enable this option for this lab.

Note that if you have installed a 3rd Party anti-virus software, this option will be disabled. In this case, you can control the firewall settings only through the anti-virus software.

Select the back arrow button to return to the Firewall and network protection window.

Public network details
Click Allow an app through firewall.
Allow an app through firewall highlighted on Firewall & network protection window
Scroll to google Chrome OR Mozilla Firefox. Observe in the screenshot below that the current configuration allows for Firefox to communicate on the Private network only but denies it from communicating on the Public network.
Allowed apps to communicate through Windows Defender Firewall list highlights Firefox
Click the Public box next to Firefox to allow Firefox to communicate through the Public network as well. A checkmark will appear. Click OK to return to the Firewall & network protection screen. Users will now be able to use Mozilla Firefox on the public network.
Allowing Mozilla Firefox to be used on the public network

Exercise 2: Configure Firewall Rules using Windows Defender Firewall with Advanced Security
The first exercise is based in the consumer-friendly version of Windows Defender Firewall – a simplified interface ideal for a single device in a home setting. In this exercise, we will look at Windows Defender Firewall with Advanced Security. This advanced view provides more in-depth options for configuration. All Windows Firewall rules, and their details, are stored here, allowing you to edit configurations for each rule or exception.

For this lab, we want to use Windows Defender Firewall with Advanced Security to edit an existing firewall rule. We want to enforce the following rules:

Allow the connection for Key Management Service on the Domain and Private network.
Deny the connection for Key Management Service on the Public network.
Select Advanced settings on the Firewall & network protection screen.

Advanced settings on Firewall & network protection window

Here you will see an Overview in the center panel. Make special note of the two rule types listed on the left panel:

Inbound rules: Inbound rules determine what traffic is allowed to the computer.
Outbound rules: Outbound rules determine what traffic is allowed to leave the computer.
Connection security rules
Monitoring
Each of these rules can be configured to filter traffic based on computers, users, applications, ports, protocols, and so on.
Click Inbound rules.

Rule types for Firewall & network protection, Advanced settings
Here you will see a long list of inbound rules. Note that some of the rules have a green checkmark next to them. This indicates that the rule is enabled to allow inbound communication. The rules without a checkmark are available for use but are not enabled.
Inbound rules available for Firewall settings

Scroll to the Key Management Service inbound rule in the Overview panel of Windows Defender Firewall with Advanced Security. Note the following:
The policy is currently not enabled (the Enabled column says No.)
If enabled, the rule would allow communication (the Action column says Allow.)

Double-click this rule.
Key Management Service inbound rule details

Here you will see the details of this rule. You will note that the General tab includes the name of the rule, a description of the rule, and whether the rule has been allowed or blocked. In this case, the connection is allowed. Click the Advanced tab.
Key Management Service (TCP-In) Properties and Allow the connection selected

Here you will see which profiles the rule applies to. In this case, Domain, Private and Public are all selected.
Key Management Service (TCP-In) Properties, Advanced tab shows Domain, Private, and Public profiles this rule applies to

Because we want to allow communication only with the domain and private networks, For Public this box should not have a checkmark. Next, click Apply, then click Ok.
Key Management Service (TCP-In) Properties, Advanced tab shows Public profile removed from rule

Now we will create an inbound rule that blocks communication with the public network. Since the new rule will be similar to the last, we will copy the existing rule. Right-click the Key Management Service (TCP-In) inbound rule and click Copy. Press Ctrl+V to paste.
Copy the Key Management Service (TCP-In) rule and paste to create a new rule

You will now see a second Key Management Service (TCP-In) inbound rule. Double-click the second rule to open the **Key Management Service *TCP-IN) Properties.
Open the new second Key Management Service (TCP-In) rule

Since we want to block connection with the public network, select Block the connection on the General tab. Click Apply.
Key Management Service (TCP-In) Properties, apply Block the connection on the General tab and apply

Click the Advanced tab.
Advanced tab of the Key Management Service (TCP-In) Properties rule

Click the Domain and Private boxes to remove the checkmarks. Click the Public to add the checkmark. Click Ok.
Remove the Domain and Private settings for the Key Management Service (TCP-In) rule

The Overview panel will show your changes. Right-click each Key Management Service (TCP-In) rule and click Enable rule.
Enable the Key Management Service (TCP-In) Domain, Private and Key Management Service (TCP-In) Public rules

Now you will see that a green checkmark appears next to the first rule indicating that the rule allowing communication is enabled. A circle with a line through it appears next to the second rule indicating that the rule blocking communication is enabled.
Key Management Service (TCP-In) rules status

Practice Problem
Problem: Configure Firewall Rule
Use Windows Defender Firewall with Advanced Security to block Windows Remote Management on the Public network.

Click here for a hint.
Follow the instructions in Exercise 2.

Click here for the solution.
*Click Windows Start button. Click Windows Security. Click Firewall & network protection. Click Advanced settings. First, select Inbound Rules and scroll down to Windows Remote Management (HTTP-In), inside that update rules. You will see two entries. One is for the domain network and the other is for the public network. Double-click Windows Remote Management (HTTP-In) for the public network. Click Block the connection. Click Ok.*
