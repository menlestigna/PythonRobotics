By default, Search-Mailbox is available only in the Mailbox Search or Mailbox Import Export roles, and these roles aren't assigned to any role groups. To use this cmdlet, you need to add one or both of the roles to a role group (for example, the Organization Management role group). Only the Mailbox Import Export role gives you access to the DeleteContent parameter. For more information about adding roles to role groups, see Add a role to a role group.
 
This example searches April Stewart's mailbox for messages that contain the phrase "Your bank statement" in the subject and logs the result in the SearchAndDeleteLog folder in the administrator's mailbox. Messages aren't copied to the target mailbox.
 
**Download ✶ [https://eninlili.blogspot.com/?file=2A0Pq3](https://eninlili.blogspot.com/?file=2A0Pq3)**


 
This example searches April Stewart's mailbox for messages that contain the phrase "Your bank statement" in the subject and deletes the messages from the source mailbox. You have to be assigned the Mailbox Import Export management role to use the DeleteContent switch.
 
This example searches all mailboxes in your organization for messages that contain the words "election", "candidate", or "vote". The search results are copied to the Discovery Search Mailbox in the folder AllMailboxes-Election.
 
**Note**: You need to be assigned the Mailbox Import Export management role to use this switch. By default, this role isn't assigned to any role group (including Organization Management). Typically, you assign a role to a built-in or custom role group.
 
When you use this switch with the TargetMailbox parameter, messages are copied to the target mailbox and removed from the source mailbox. If you set the logging level for the search to Basic or Full, you must specify a target mailbox and a target folder to place the log in. To delete messages from the source mailbox without copying them to the target mailbox, don't specify the TargetMailbox, TargetFolder, and LogLevel parameters.
 
The DomainController parameter specifies the domain controller that's used by this cmdlet to read data from or write data to Active Directory. You identify the domain controller by its fully qualified domain name (FQDN). For example, dc01.contoso.com.

When you included this parameter, an email message is created and sent to the mailbox specified by the TargetMailbox parameter. The log file (which is a CSV-formatted file named Search Results.csv) is attached to this email message, and will be located in the folder specified by the TargetFolder parameter. The log file contains a row for each message that's included in the search results when you run the Search-Mailbox cmdlet.
 
The SearchDumpster switch specifies whether to include the Recoverable Items folder in the search. The Recoverable items folder stores items that were deleted from the Deleted Items folder or items that were hard-deleted until they're purged from the mailbox database.
 
The SearchQuery parameter specifies a search string or a query formatted using Keyword Query Language (KQL). For more information about KQL in Exchange, see Message properties and search operators for In-Place eDiscovery.
 
The WhatIf switch simulates the actions of the command. You can use this switch to view the changes that would occur without actually applying those changes. You don't need to specify a value with this switch.
 
Some USPS services require identity verification. If you can't verify your identity online (or prefer not to), follow your instructions and bring acceptable ID and any required documents or barcodes.
 
Most collection boxes are freestanding mailboxes such as the familiar USPS Blue Box, special white mailboxes for prepaid Priority Mail Express items, lobby drop-off slots, or office building mail chutes. Pickup times are posted on the box label.
 
Contract Postal Units (CPUs) are located within existing businesses. While not freestanding Post Office locations, CPUs provide a full range of USPS retail products and services at regular USPS prices.
 
A few kiosks are in large shopping malls. Most kiosks are in Post Office lobbies and offer many of the services available at the full-service Post Office counter. You can buy stamps, weigh packages, and print Priority Mail and Priority Mail Express shipping labels at kiosks. Bring packing tape and you can ship your items in our free boxes.
 
One of our users showed me that there are some emails in her mailbox which can't be found by using search, nor in the Outlook 2013 rich client (in Online mode), neither in OWA. Tried to search for various texts and properties from those emails, but they was just 'invisible' for search.
 
It seems this, submitting a move request for that mailbox is the recommended way to force reindexing an ExO hosted mailbox. Once the move operation has completed (it takes a few hours depending on the mailbox size, progress can be checked with Get-MoveRequestStatistics) the mailbox got re-indexed, which fixed the search.
 
In our case there appeared to a small 3-month window in which messages were missing from the search results. SO we would see some older messages, as well as very recent messages. However, any that were within the three-month window would not be returned when searching.
 
This might have something to do with our migration process to Office 365. We used BitTitan to perform a pre-stage migration that moved all mail older than 90 days. Then after we switched to Office 365 live, we performed a full migration that picked up all mail within the most recent 90-day time frame. It seemed that these messages were the messages that did not get indexed by the search engine.
 
The move process might take a few hours to even a day or two to complete. Mailboxes remain accessible and usable during this operation, so users should not experience any issues if the move is processing during working hours.
 
It appears that this is what needs to be done to our EOL server, but as I am not familiar with the New-MoveRequest command, I want to make sure I'm not about to do something wrong. We've been fully migrated from a local Exchange Server to EOL for quite some time now. I don't want to move our mailboxes anywhere or cause any issues. I just need to repair what appears to be an indexing issue affecting a user's mailbox search functionality (specifically my own mailbox).
 
Thanks for the affirmation. I ran the process without incident, but it unfortunately did not resolve the search issue I am having. I tried compacting the ost from without Outlook to see if that might resolve the issue, but it didn't seem to make any progress after 12 hours of running. Not sure if this duration is typical or not.
 
Interestingly, I let the oct compact process run to completion over the weekend and rebuilt the index. Now, the Outlook client seems to be properly returning search results. However, in OWA, it is still an issue.
 
We have people using shared mailboxes, their outlook is in cached mode for the main inbox but for shared mailboxes the cache is off. When they try to search in a shared mailbox, they are getting different results in "Current mailbox" and "Subfolders" even though the message that they are searching for is within the search scope in inbox.... when disabling cached mode for the user profile the search works fine.... It doesn't make sense because "download shared folders" unchecked means that there's no cache for shared mailboxes already so unchecking "Use cached exchange mode to download email to an outlook data file" shouldn't affect shared mailboxes.... Of course Microsoft support is so bad....
 
One of my machines fixed itself after a weekend and the shared mailbox seemed to have reset itself (opened blank and empty, then slowly repopulated) but I cannot find a way to force this fix on another affected machine.
 
So I cannot search both mailboxes at the same time - and it's very convoluted to do a search. Is there some setting that's wrong or does this suggest the way the mailbox is set up on the server is causing problems... or something else?
 
Based on my test, I have done several tests in my Outlook 365 (version is as shown in the below figure) with two personal accounts configured and i could search emails from all mailboxes successfully, which didn't reproduce you issue. It's suggested that you could try to configure two personal accounts to test if there're any differences.
 
If it's a shared mailbox, as I know, **to search a Shared Mailbox, we need to click the mailbox and use the Current Folder scope.** This is by design. To work around this issue, you can add the Shared Mailbox as a secondary Exchange account to the profile.
 
Thank you for your clarification. Do you recon where you got that information from the screenshot from? Microsoft in my opinion really broke searching in Outlook. Searching across multiple auto-mapped mailboxes doesn't work (while the option is visible in Outlook, confusing), it's just not a reliable expirience in any way unfortunately. Adding mailboxes as an account in Outlook is not always an option, specially not when these are user mailboxes, then you would have to deal with MFA and password changes which might become difficult to maintain aswel.
 
If you are planning to use this for a large set of users, you will likely run into throttling limits, so it only applicable for smaller teams. For larger teams/organization-wide contacts, Public folder based contact list might work: -it.com/blog/create-a-company-shared-contacts-folder-in-office-365/
 
I ran into a similar issue with shared mailboxes. 2 users accessing the same shared mailbox. 1 user could use the outlook search function and search contents of the shared mailbox and the other user could not. Same OS and office version, same exchange settings and permissions. Advice I received included rebuilding the index for the emails/ost, as well as locating the