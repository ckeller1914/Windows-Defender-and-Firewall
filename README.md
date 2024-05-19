# Windows Defender Firewall

## Objectives

   ### Windows Defender Firewall is a host-based software firewall included with the Windows operating system. This guide will help you configure firewall rules using Windows Defender Firewall with Advanced Security.

## Skills Acquired

   ### Configuring Firewall Rules | Managing Inbound Rules | Applying Rule Properties | Enabling and Disabling Rules

## Task: Configure Firewall Rules using Windows Defender Firewall with Advanced Security

   ###  For this lab, we will use Windows Defender Firewall with Advanced Security to edit existing firewall rules to:

   #### -Allow the connection for Key Management Service on the Domain and Private network.

   #### -Deny the connection for Key Management Service on the Public network.
      
   #### -Allow the connection for Windows Remote Management (HTTP-In).
      
   #### -Deny the connection for Windows Remote Management (HTTP-In).

## Steps

   ### 1) Open the Windows Defender Firewall with Advanced Security by selecting "Advanced settings" on the "Firewall & network protection" screen. 

![Advanced Settings](https://github.com/ckeller1914/Windows-Defender-and-Firewall/assets/116524804/3dcdb50e-8a6d-40ef-9b0e-92c75fab2efb)


   ### 2) In the "Advanced settings," you will see an Overview panel. Take note of the rule types listed on the left panel: Inbound rules and Outbound rules.
   
   
![InOut](https://github.com/ckeller1914/Windows-Defender-and-Firewall/assets/116524804/ffc04a11-dcce-4059-83d5-7e3d0182acae)

### 3) Click on "Inbound rules" to see the list of inbound rules available for Firewall settings.

![inboundnew](https://github.com/ckeller1914/Windows-Defender-and-Firewall/assets/116524804/b31aed82-39e7-45ae-839a-81a5dc816591)

### 4) Scroll to find the "Key Management Service" inbound rule in the Overview panel.

   #### -Note that the policy is currently not enabled.
   
   #### -Double-click this rule to open its properties.


![key management](https://github.com/ckeller1914/Windows-Defender-and-Firewall/assets/116524804/09fc0e60-f826-44e1-9e56-4a5e90e3446d)

### 5) Here you will see the details of this rule. Go to Key Management Service (TCP-In) Properties and Allow the connection selected.

   
![General](https://github.com/ckeller1914/Windows-Defender-and-Firewall/assets/116524804/a38d840e-531d-414a-af27-d6ad42ef8547)

### 6) In the rule properties, go to the "Advanced" tab. Here, you will see which profiles the rule applies to (Domain, Private, Public). Uncheck "Public" and click "Apply," then "OK."


   
![advance](https://github.com/ckeller1914/Windows-Defender-and-Firewall/assets/116524804/e19e5bae-9309-4a43-8d5f-c0361700d092)


 ### 7) Because we want to allow communication only with the domain and private networks, For Public this box should not have a checkmark. Next, click Apply, then click Ok.
 
  #### -Key Management Service (TCP-In) Properties, Advanced tab shows Public profile removed from rule

 ### 8) To create an inbound rule that blocks communication with the public network, copy the existing rule:

   #### -Right-click the Key Management Service (TCP-In) inbound rule and click "Copy."
   
   #### -Press Ctrl+V to paste.

 ### -Copy the Key Management Service (TCP-In) rule and paste to create a new rule

![9](https://github.com/ckeller1914/Windows-Defender-and-Firewall/assets/116524804/33ee4cd3-30a5-4921-b095-e0fa1d7350d1)


### 9) You will now see a second Key Management Service (TCP-In) inbound rule. Double-click the second rule to open the **Key Management Service *TCP-IN) Properties.

![10](https://github.com/ckeller1914/Windows-Defender-and-Firewall/assets/116524804/5f42fd8f-4fa5-46fd-902c-7fea25bc45cf)


### 10) Since we want to block connection with the public network, select Block the connection on the General tab. Click Apply.

![block](https://github.com/ckeller1914/Windows-Defender-and-Firewall/assets/116524804/3849ed4a-6017-4a49-ad59-39350c11894e)


 ###  11) Go to Key Management Service (TCP-In) Properties, apply Block the connection on the General tab and apply

 ### 12) In the Advanced tab. Click the Domain and Private boxes to remove the checkmarks. Click the Public to add the checkmark. Click Ok.

![public](https://github.com/ckeller1914/Windows-Defender-and-Firewall/assets/116524804/018edf85-6e9e-4772-b5e9-f4ac8ff41a8c)


 ### 13) Remove the Domain and Private settings for the Key Management Service (TCP-In) rule
   

 ### 14) Right-click each Key Management Service (TCP-In) rule and click Enable rule. Enable the Key Management Service (TCP-In) Domain, Private and Key Management Service (TCP-In) Public rules


 ### 15) Now you will see that a green checkmark appears next to the first rule indicating that the rule allowing communication is enabled. A circle with a line through it appears next to the second rule indicating that the rule blocking communication is enabled.

![keyquest](https://github.com/ckeller1914/Windows-Defender-and-Firewall/assets/116524804/18b7cd55-3e12-4d07-969f-3fa1b40e0f2a)

   
### 16) Use Windows Defender Firewall with Advanced Security to block Windows Remote Management on the Public network.

### 17) First, select Inbound Rules and scroll down to Windows Remote Management (HTTP-In), inside that update rules. You will see two entries. One is for the domain network and the other is for the public network. Double-click Windows Remote Management (HTTP-In) for the public network.


![remote](https://github.com/ckeller1914/Windows-Defender-and-Firewall/assets/116524804/bf2124ac-69a0-49c9-99f0-728041062ec9)


### 18) Click Block the connection. Click Ok.
