# Applying The CIA Triad To Your Enterprise File Transfer

### Confidentiality
<p> This refers to restricting access to or knowledge of certain pieces of information to certain idividuals. A few reasons you might want to do so are as follows. 
  <ul>
    <li> a company migh tnot want competitors to know its trade secrets, personnel salaries, list of customers, products in development, or sales and marketing plans. </li>
    <li> a law firm  might want to preserve attorney-client privilege </li>
    <li> a healthcare organization may want to secure ePHI and comply with HIPAA/HITECH requirements </li>
    <li> trading partners might want to keep transaction details between themselves </li>
  </ul>
</p>

### Integrity
<p> Preventing data from being tampered with. This is critical for businesses where data being tampered with could result in financial losses </p>

### Availability
<p> This ensures that the data is accessible when you need it. </p>

## Technical Solutions for achieving confidentiality in enterprise file transfers
<p> Encryption can be broken into two general concepts; protection while data is at rest, and while data is in transit.

  Data -in-Transit: This is usually achieved through solution like SSL (FTPS, HTTPS, WebDAVs) or SSH (SFTP). 
  
  Another method to help secure data is authenticaetion, such as 2-factor authentication.
</p>

## Integrity in enterprise file transfers
<p> You can use hash functions and digital signatures to maintain the integrity of your files in transfer. 
</p>



source: https://www.jscape.com/blog/implementing-the-cia-triad-when-transferring-files-through-the-internet
