---
title: check-storages-usage-reports
displayName: View statistics
published: true
order: 80
toc:
---
For storage billing we use the following metrics:

*   used space,
*   requests,
*   traffic.

The data for all metrics is available in the Statistics section. It can be requested for a day, two days, week, month, year, or you can choose a custom time period in the calendar on the right. The data can also be sorted by storage types (s3 or sftp), locations, and names.

<img src="https://support.gcore.com/hc/article_attachments/360003274157/Screenshot_70.png" alt="Screenshot_70.png">

Statistics appear in the Control panel within a couple of hours after storage creation. For the s3 storages in the Global 2 location, it always comes a day later. 

On the graphs we show aggregated data: used storage space gets measured every hour, the collected data is analyzed and shown as max and average usage values for a day. The longer the requested time period the more operations has to be done to represent the data so requests for long time periods (a year, for example) can take some time to get processed.

About 350 kB of SFTP storage space is taken by system files: ssh keys, empty directories, robot.txt file. If you created a storage but haven't uploaded anything to it, the statistics will show the space taken by the system files. Keep in mind that in invoices we round the value of used space to the whole number of GB.