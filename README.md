Objectives


Windows Defender Firewall is a host-based software firewall that is included with the Windows operating system. Throughout this lab I learned to configure firewall rules using Windows Defender Firewall with Advanced Security.



Task: Configure Firewall Rules using Windows Defender Firewall with Advanced Security


For this lab, we want to use Windows Defender Firewall with Advanced Security to edit an existing firewall rule. We want to enforce the following rules:

Allow the connection for Key Management Service on the Domain and Private network.
Deny the connection for Key Management Service on the Public network.

1. Select Advanced settings on the Firewall & network protection screen.

Advanced settings on Firewall & network protection window

![Advanced Settings](https://github.com/ckeller1914/Windows-Defender-and-Firewall/assets/116524804/3dcdb50e-8a6d-40ef-9b0e-92c75fab2efb)


2. Here you will see an Overview in the center panel. Make special note of the two rule types listed on the left panel:

Inbound rules: Inbound rules determine what traffic is allowed to the computer.
Outbound rules: Outbound rules determine what traffic is allowed to leave the computer.
Connection security rules
Monitoring
Each of these rules can be configured to filter traffic based on computers, users, applications, ports, protocols, and so on.

![InOut](https://github.com/ckeller1914/Windows-Defender-and-Firewall/assets/116524804/ffc04a11-dcce-4059-83d5-7e3d0182acae)


Click Inbound rules.

Rule types for Firewall & network protection, Advanced settings

3. Here you will see a long list of inbound rules. Note that some of the rules have a green checkmark next to them. This indicates that the rule is enabled to allow inbound communication. The rules without a checkmark are available for use but are not enabled.
Inbound rules available for Firewall settings

![inboundnew](https://github.com/ckeller1914/Windows-Defender-and-Firewall/assets/116524804/b31aed82-39e7-45ae-839a-81a5dc816591)



5. Scroll to the Key Management Service inbound rule in the Overview panel of Windows Defender Firewall with Advanced Security. Note the following:
The policy is currently not enabled (the Enabled column says No.)
If enabled, the rule would allow communication (the Action column says Allow.)

Double-click this rule.
Key Management Service inbound rule details

![key management](https://github.com/ckeller1914/Windows-Defender-and-Firewall/assets/116524804/09fc0e60-f826-44e1-9e56-4a5e90e3446d)

5. Here you will see the details of this rule. You will note that the General tab includes the name of the rule, a description of the rule, and whether the rule has been allowed or blocked. In this case, the connection is allowed.
   
![General](https://github.com/ckeller1914/Windows-Defender-and-Firewall/assets/116524804/a38d840e-531d-414a-af27-d6ad42ef8547)


7. Click the Advanced tab.
Key Management Service (TCP-In) Properties and Allow the connection selected

9. Here you will see which profiles the rule applies to. In this case, Domain, Private and Public are all selected.
Key Management Service (TCP-In) Properties, Advanced tab shows Domain, Private, and Public profiles this rule applies to

![advance](https://github.com/ckeller1914/Windows-Defender-and-Firewall/assets/116524804/e19e5bae-9309-4a43-8d5f-c0361700d092)


10. Because we want to allow communication only with the domain and private networks, For Public this box should not have a checkmark. Next, click Apply, then click Ok.
Key Management Service (TCP-In) Properties, Advanced tab shows Public profile removed from rule

12. Now we will create an inbound rule that blocks communication with the public network. Since the new rule will be similar to the last, we will copy the existing rule. Right-click the Key Management Service (TCP-In) inbound rule and click Copy. Press Ctrl+V to paste.

![9](https://github.com/ckeller1914/Windows-Defender-and-Firewall/assets/116524804/33ee4cd3-30a5-4921-b095-e0fa1d7350d1)


Copy the Key Management Service (TCP-In) rule and paste to create a new rule

13. You will now see a second Key Management Service (TCP-In) inbound rule. Double-click the second rule to open the **Key Management Service *TCP-IN) Properties.

![10](https://github.com/ckeller1914/Windows-Defender-and-Firewall/assets/116524804/5f42fd8f-4fa5-46fd-902c-7fea25bc45cf)


Open the new second Key Management Service (TCP-In) rule

14. Since we want to block connection with the public network, select Block the connection on the General tab. Click Apply.

![block](https://github.com/ckeller1914/Windows-Defender-and-Firewall/assets/116524804/3849ed4a-6017-4a49-ad59-39350c11894e)


Key Management Service (TCP-In) Properties, apply Block the connection on the General tab and apply

15. Click the Advanced tab.
Advanced tab of the Key Management Service (TCP-In) Properties rule

16. Click the Domain and Private boxes to remove the checkmarks. Click the Public to add the checkmark. Click Ok.

![public](https://github.com/ckeller1914/Windows-Defender-and-Firewall/assets/116524804/018edf85-6e9e-4772-b5e9-f4ac8ff41a8c)


Remove the Domain and Private settings for the Key Management Service (TCP-In) rule

17. The Overview panel will show your changes. Right-click each Key Management Service (TCP-In) rule and click Enable rule.



Enable the Key Management Service (TCP-In) Domain, Private and Key Management Service (TCP-In) Public rules

18. Now you will see that a green checkmark appears next to the first rule indicating that the rule allowing communication is enabled. A circle with a line through it appears next to the second rule indicating that the rule blocking communication is enabled.

![keyquest](https://github.com/ckeller1914/Windows-Defender-and-Firewall/assets/116524804/18b7cd55-3e12-4d07-969f-3fa1b40e0f2a)


Key Management Service (TCP-In) rules status

19. Use Windows Defender Firewall with Advanced Security to block Windows Remote Management on the Public network.


16.Click Windows Start button. Click Windows Security. Click Firewall & network protection. Click Advanced settings. 

17. First, select Inbound Rules and scroll down to Windows Remote Management (HTTP-In), inside that update rules. You will see two entries. One is for the domain network and the other is for the public network. Double-click Windows Remote Management (HTTP-In) for the public network.
18.
19.![remote](https://github.com/ckeller1914/Windows-Defender-and-Firewall/assets/116524804/bf2124ac-69a0-49c9-99f0-728041062ec9)

20.
21. Click Block the connection. Click Ok.
