---
title: behavioral-waf
displayName: Behavioral WAF
published: true
order: 40
toc:
   --1--Configure policy group: "configure-policy-group"
   --2--Anti-spam: "anti-spam"
   --2--Probing and forced browsing: "probing-and-forced-browsing"
   --2--Obfuscated attacks and zero-day mitigation: "obfuscated-attacks-and-zero-day-mitigation"
   --2--Repeated violations: "repeated-violations"
   --2--Brute-force protection: "brute-force-protection"
pageTitle: Set up Behavioral WAF policy for your domain | Gcore
pageDescription: Learn how to enable and customize Behavioral WAF policy.
---
# Behavioral WAF

The Web Application and API Protection (WAAP) includes a Behavioral WAF policy group that helps prevent malicious attacks on your websites. The policy group contains a set of sophisticated user behavior and reputation analysis policies that inspect traffic and defend your website against threats such as spamming or brute force attacks. 

<alert-element type="info" title="Info">
 
This policy group is available in the <a href="https://gcore.com/docs/waap/billing#pro" target="_blank">Pro</a> and <a href="https://gcore.com/docs/waap/billing#enterprise" target="_blank">Enterprise</a> plans.
 
</alert-element> 

## Configure policy group 

You can review the Behavioral WAF policy group and enable or disable its policies in the <a href="https://accounts.gcore.com/reports/dashboard" target="_blank">Gcore Customer Portal</a>: 

1\. Navigate to **WAAP** > **Domains**. 

<img src="https://assets.gcore.pro/docs/waap/waap-policies/domains-waap-page.png" alt="Domains page in the Customer Portal" width="80%">

2\. Find the domain where you want to configure the policy and click the domain name to open it.  

3\. On the **Policies** page that opens, click **Behavioral WAAP** to expand the section and adjust the policies. 

<img src="https://assets.gcore.pro/docs/waap/waap-policies/behavioral-waf/behavioral-waf.png" alt="WAF policies page with the highlighted ehavioral WAF policy" width="80%">

<alert-element type="info" title="Info">

All behavioral WAF policies are enabled by default. To disable a policy, turn on the toggle near that policy. 

</alert-element>

### Anti-spam 

Use CAPTCHA and JavaScript validation when user activity during a session suggests aggressive use of forms to, for instance, generate new accounts or post spam content. 

### Probing and forced browsing 

Use CAPTCHA and JavaScript validation to challenge brute-forced requests on random URLs, which might aim to discover your web application’s  structure and hidden directories. Requests that fail to pass the validation will be blocked.  

### Obfuscated attacks and zero-day mitigation 

Block clients that perform multiple injection attacks. 

### Repeated violations 

Present with CAPTCHA or block those clients that failed to answer a previously displayed challenge. Requests that fail to pass the validation will be blocked. 

### Brute-force protection 

Present users with CAPTCHA when there’s an attempt to guess usernames and passwords on web login forms. If the client fails to pass the validation after a few attempts, the request will be blocked.