Dean Weiss
1 December 2022

# What is Mimikatz?

<p>
Mimikatz is an open-source application that allows users to view and save authentication credentials, such as Kerberos tickets.
  
It is commonly used to steal credentials and escalate privileges. Pen testers also use it to detect exploits so that they can fix them.
  
### What can it do?
  
- Pass-the-hash: Windows used to store password data in an NTLM hash. Attackers use Mimikatz to pass that exact hash string to the target computer to log in. Attackers don’t even need to crack the password — they just need to use the hash string as-is. It’s the equivalent of finding the master key to a building on the lobby floor. You need just that one key to get into all the doors.
- Pass-the-ticket: Newer versions of Windows store password data in a construct called a ticket. Mimikatz provides functionality for a user to pass a Kerberos ticket to another computer and log in with that user’s ticket. It’s very similar to the pass-the-hash method.
Overpass-the-hash (pass-the-key): Yet another flavor of the pass-the-hash, but this technique passes a unique key obtained from a domain controller to impersonate a user.
Kerberoast golden tickets: This is a pass-the-ticket attack, but it’s a specific ticket for a hidden account called KRBTGT, which is the account that encrypts all of the other tickets. A golden ticket provides you with non-expiring domain admin credentials to any computer on the network.
- Kerberoast silver tickets: Another pass-the-ticket, but a silver ticket takes advantage of a feature in Windows that makes it easy for you to use services on the network. Kerberos grants a user a ticket-granting server (TGS) ticket, and a user can use that ticket to authentic to service accounts on the network. Microsoft doesn’t always check a TGS after it’s issued, so it’s easy to slip past any safeguards.
- Pass-the-cache: Finally an attack that doesn’t take advantage of Windows! A pass-the-cache attack is generally the same as a pass-the-ticket, but this one uses the saved and encrypted login data on a Mac/UNIX/Linux system.  
</p>

  
### Defend Against it

- Restrict admin privileges. This can be done by limiting admin privileges to only users who need them.
- Disable password-caching. Windows caches password hashes that were recently used through their system registry. Mimikatz can then gain access to these cached passwords, which is why it’s important to change your default settings to cache zero recent passwords. This can be accessed through Windows Settings > Local Policy > Security Options > Interactive Logon.  
- Turn off debug privileges. Windows’ default settings allows local admins to debug the system, which Mimikatz can exploit. Turning off debugging privileges on machines is a best practice to safeguard your system.  
- Configure additional local security authority (LSA) protection. Upgrading to Windows 10 can help mitigate the types of authentication attacks that Mimikatz enables. However, when this isn’t possible, Microsoft has additional LSA configuration items that help reduce the attack surface area.

source: https://www.varonis.com/blog/what-is-mimikatz
