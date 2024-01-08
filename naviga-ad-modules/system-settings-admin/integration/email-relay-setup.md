---
description: >-
  This is what you need to do on your end for emails to be successfully sent
  from Naviga Ad to your customers.
---

# Email Relay Setup

## **Outbound Emails via Naviga**

<img src="../../../.gitbook/assets/image (7) (1).png" alt="" data-size="line"> **Customer needs this in their Mail SPF TXT record for ALL email domains they think might send**

An SPF record is a DNS record that the customer has on their end.

They need to add in the External IPs and/or the Domain of our mail relay so that when THEIR customer receives (IP is more important) an email from our mail relay- those two domains can talk to each other over the internet and the recipients mail domain can ask the Naviga Customers Mail domain if we are a valid sender on their behalf.

If there is no reference to us as a valid sender the mail MIGHT be:

1. Rejected
2. Considered SPAM
3. Be postponed
4. Accepted

### <mark style="background-color:yellow;">**Customers on AWS-EAST and AWS-WEST use this:**</mark>

v=spf1 **ip4:52.6.112.187 include:navigacloud.com** \~all

### <mark style="background-color:yellow;">**EU - UK - Asia - Africa ONLY - this is the European Relay on AWS-Ireland:**</mark>

v=spf1 **ip4:52.30.213.6 include:navigacloud.com** \~all

### <mark style="background-color:yellow;">**Customers on AWS-Canada use this:**</mark>

v=spf1 ip4: 52.60.125.222 include:navigacloud.com \~all

### **DKIM Signature - An additional advanced way of adding Email Validation**

We, Naviga, can provide a DKIM Hash for any domain and provide it to the customer which they then enter on their DNS. The customer can let their Implementation Specialist know so they can ask hosting for a DKIM hash and we can provide this.

{% hint style="info" %}
**\*\*\*Please note: this will need to be for ALL Email Domains and all Domains will need the SPF record set as stated above.**
{% endhint %}

What is DKIM?

The DKIM signature will be generated in a unique textual string, the ‘hash value’. Before sending the email, the hash value is encrypted with a private key, the DKIM signature. Only the sender has access to this private key. When the email is encrypted the email is sent with this DKIM signature.

Email receivers, like Gmail and Microsoft (Hotmail, Outlook etc), detect the DKIM signature. This DKIM signature reveals which domain was used to sign the email in the encryption process. To validate the DKIM signature, the email receiver will run a DNS query to search for the public key for that domain. The variables provided in the DKIM signature are used to determine where to look for this key. If the key was found, it can be used to decrypt the DKIM signature back the to original hash values. These values are compared to the new values retrieved from the received mail. If they match, the DKIM was valid.

**Example**

default.\_domainkey IN TXT "v=DKIM1; k=rsa;\
p=MIGfMA0GCSqGSIb3DQEBAQUAA4GNADCBiQKBgQC0cbbwbfCs2jfzZ+6a3ISOED+oy138kCK7B+ZhwtqvVDCfgmJ0qdQYbPq1EefXK/37D4p3FZRUpe/SakS63uzEwxnvm6+ruWTsWeET2Xz2F5vp8YhSPa/ueSqjcyK8WQilw0Y/gJCEAjl40oOObh091p2/j7SXN7UvjkQ1oImVGQIDAQAB"
