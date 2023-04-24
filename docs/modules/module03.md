# Module 03 - Hot, warm, and cold data storage

When it comes to data storage, it can be easy to get lost in a sea of terms and acronyms. Which is better, SSD or HDD? Cloud or hybrid cloud? A cloud of what? Like many things in life, the answer to all of these questions is simple - It depends!  

While storage hardware considerations can be tricky to navigate, it's worth investing time and energy in choosing which storage solutions you need early in the research lifecycle. This is because a sound data storage strategy is your first line of defence against data loss in the event of natural and/or human-derived disaster. In this Module, we’ll briefly explore three classes of storage types: hot, warm and cold, and how storage type may inform data management strategies. Once you find what storage temperatures best suit your needs, we recommend talking to your [eResearch support team](https://genomicsaotearoa.github.io/data-management-resources/modules/module04/) to find which hardware solutions best fit the bill.  

The differences between storage types have less to do with spice level or temperature and more to do with the speed of read and write access. The hotter the storage, the faster the speed of access. However, the need for speed comes at a cost... literally. The faster your read/write capability, the more expensive it is. When choosing hardware, striking a balance between the intended use and financial resource will go a long way in helping you identify the appropriate hardware. For example, you will want the fastest access possible for data analysis, and therefore the hottest storage option. For data that is accessed intermittently or stored in the long-term, colder options with slower access and lower costs will do the trick.  

<figure>
  <center><img src="https://github.com/GenomicsAotearoa/data-management-resources/blob/main/docs/figures/Hot-warm-cold-storage-transparent.png?raw=true" alt="Data storage temperatures" style="width:85%" class="center"></center>
  <figcaption>
    A comparison of factors associated with different data storage temperatures, from hot to cold.
  </figcaption>
</figure>

For consistency within research groups, it may be helpful to decide as a group which data/file types require which storage temperatures to maximise efficiency, maintain data security, and meet the needs specified in DMPs. Regardless of how hot or cold your storage is, it’s important to make sure sufficient metadata (see [Module 07](https://genomicsaotearoa.github.io/data-management-resources/modules/module07/)) is collated alongside your data to support other users (including future you!) in navigating directories and understanding file contents.  

## What is hot storage? :fontawesome-solid-sun: 

In the case of hot storage, we generally mean storage for data that you're actively analysing that requires immediate read/write access. Data is generally stored locally to where it is being analysed. One example of usage of hot storage would be for data actively in use for genome alignment and variant discovery.

As a general rule of thumb, hot storage should be considered a temporary home for data. This is because it is a relatively expensive resource that is best suited to holding data for active use, and so more focus is placed on performance. In an HPC (High Performance Computing) environment where you want to squeeze out maximum performance, hot storage may not be backed up, as ‘quiet time’ to do so is rare, and performance will take a hit during backing up.  

Taking all this into consideration, hot storage is not a good place for keeping your data in the long term - there may not be enough room and it is not safe. You should keep a master copy on a cooler form of storage where safety and integrity are ensured and only copy what you need onto the hot storage for your compute. As you generate important results, these should be copied from hot storage to cooler storage at the first opportunity.

## What is warm storage? <i class="fas fa-cloud-sun"></i>

Next up is warm storage, which is best suited to store data for intermittent access. It is generally less expensive than drives used for hot storage. While access to data is slower, it is relatively immediate and is a good staging place for data that you use regularly. Analysis that does not require HPC can take place here, and this storage can usually be backed up. Data that you might consider putting on warm storage includes files that take a long time to generate and are likely to be reused, such as BAM alignment files used for variant discovery. 

A typical drive in a personal machine issued by an institute is warm. But note - although some institutes will issue faster drives, you’ll notice these have low capacity and you will likely need to rely on a form of network or cloud storage to supplement it. Network storage at your institute is more warm (to you) than hot.  

## What is cold storage? <i class="fas fa-snowflake"></i>

Finally, cold storage is largely for data that is rarely accessed or archived. For cold storage, the emphasis is placed on the most bang for your buck for capacity. With that being said cold storage comes in many varieties depending on how much money you want to spend, the capacity you need and the retrieval time you are willing to accept.  

While data in hot and warm storage is accessible immediately (in human terms), in the coldest storage access can take minutes, hours, or even days, depending on the size of the data, the technology involved and whether human intervention is needed. Cloud storage options like Dropbox and OneDrive are actually more towards the cold end of the thermometer, as data needs to be synchronised or downloaded/uploaded.

In cold storage there should also be a great emphasis on data safety and integrity. The drive will usually be backed up, and there may be data integrity checks. This means that cold storage is an excellent place for storing master copies of raw data as a safety measure.  

## The strange case of cloud storage <i class="fa-solid fa-cloud"></i>

Cloud storage systems (e.g., Dropbox, OneDrive, Google Drive, Amazon Web Services Cloud) are effectively cold if you want to use them on your machine. The primary interface for cloud storage is file transfer via a web browser meaning it is not immediately available. Some services like Google Drive or Microsoft OneDrive use their associated cloud storage directly and if you use the associated web applications, it gives the appearance of warm storage. If you are only using this on a single machine, you effectively have a folder backed up in the cloud. But if you want to share a file or use the cloud as a common drive between machines, you may notice that data may not be immediately available. Sometimes how hot or cold a storage is depends on how remote it is to you or the application that uses it.

*[DMP]: Data Management Plan
*[HDD]: Hard Disk Drive
*[SSD]: Solid State Drive
*[HPC]: High Performance Computing
*[BAM]: Binary Alignment Map. A file format used to encode aligned genomic data.
