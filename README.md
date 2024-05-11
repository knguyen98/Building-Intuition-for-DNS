# Building-Intuition-for-DNS
<img src="https://i.imgur.com/CtGfsq8.png" alt="osTicket logo"/>
</p>

<h1>Understanding DNS Fundamentals</h1>
<p>In this lab, we delve into the intricacies of DNS to enhance our comprehension of its core principles.</p>

<h2>Environments and Technologies Utilized</h2>

<ul>
  <li>Microsoft Azure (Virtual Machines/Compute)</li>
  <li>Remote Desktop</li>
  <li>DNS</li>
</ul>

<h2>Operating Systems Employed</h2>

<ul>
  <li>Windows 10 (21H2)</li>
</ul>

<h2>Prerequisites</h2>

<ul>
  <li>Active Directory Virtual Machine</li>
  <li>Client Machine joined to your domain</li>
</ul>

<h2>Step-by-Step Tutorial</h2>

<p>Let's embark on a journey to explore DNS A-Records, essential components that map hostnames to IP addresses:</p>

<ol>
  <li><strong>Creating DNS A-Records:</strong> Begin by crafting an A record on DC-1 for "mainframe," directing it to DC-1's private IP address. Without this record, attempting to ping "mainframe" would yield no response.</li>
</ol>

<div>
  <img src="https://i.imgur.com/xKePr4k.png" alt="Disk Sanitization Steps" height="80%" width="80%">
</div>
<div>
  <img src="https://i.imgur.com/yAlrhZw.png" alt="Disk Sanitization Steps" height="80%" width="80%">
</div>

<p>Subsequently, alter the record address of "mainframe" to 8.8.8.8. Although changed, the client machine might still ping the old address due to cached DNS. Use the command <code>ipconfig /flushdns</code> to clear the DNS cache.</p>

<div>
  <img src="https://i.imgur.com/KYNmZMz.png" alt="Disk Sanitization Steps" height="80%" width="80%">
</div>
<div>
  <img src="https://i.imgur.com/80ARdZu.png" alt="Disk Sanitization Steps" height="80%" width="80%">
</div>

<p>Finally, configure a CNAME record, linking the host "search" to "www.google.com." Initially, pinging "search" would fail, but after creating the CNAME record, it would resolve to www.google.com.</p>

<div>
  <img src="https://i.imgur.com/LgomfqN.png" alt="Disk Sanitization Steps" height="80%" width="80%">
</div>
<div>
  <img src="https://i.imgur.com/NovtDrd.png" alt="Disk Sanitization Steps" height="80%" width="80%">
</div>
