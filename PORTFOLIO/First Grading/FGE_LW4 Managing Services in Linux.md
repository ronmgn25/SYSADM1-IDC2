+----------------------------------+------------------------+----------+
| ![](vertopal_                    |                        |          |
| 808139c8243f45408815596a49e28422 |                        |          |
| /media/image1.png){width="2.4in" |                        |          |
| height="0.5881944444444445in"}   |                        |          |
|                                  |                        |          |
| SCHOOL OF INFORMATION AND        |                        |          |
| TECHNOLOGY                       |                        |          |
+----------------------------------+------------------------+----------+
| NAME: MAGNO, RONNIE L.           | DATE PERFORMED:        |          |
|                                  | 09/12/24               |          |
+----------------------------------+------------------------+----------+
| Section: IDC2                    | DATE SUBMITTED:        |          |
+----------------------------------+------------------------+----------+

# SYSADM1 -- Managing Services in Linux

# Requirement: 

-   A virtual machine running Linux

![](vertopal_808139c8243f45408815596a49e28422/media/image2.png){width="4.135416666666667in"
height="1.8020833333333333in"}

Complete this lab as follows:

1.  Use the service --status-all command to list all active and inactive
    services.

List down active and inactive services in the table below. Provide five
(5) services for each column.

  -----------------------------------------------------------------------
  **Active**                             **Inactive**
  -------------------------------------- --------------------------------
  procps                                 uuidd

  cron                                   bluetooth

  apport                                 sssd

  kmod                                   saned

  sysstat                                rsync
  -----------------------------------------------------------------------

SS:

![](vertopal_808139c8243f45408815596a49e28422/media/image3.png){width="4.731541994750656in"
height="3.4826093613298337in"}

2.  Start the Bluetooth service using the systemctl command.

Ex. sudo systemctl start httpd

![](vertopal_808139c8243f45408815596a49e28422/media/image4.png){width="4.359946412948381in"
height="1.1875in"}

3.  Check the status of the Bluetooth service. What is its status?

The status of Bluetooth is inactive

SS:

![](vertopal_808139c8243f45408815596a49e28422/media/image5.png){width="7.027083333333334in"
height="0.9159722222222222in"}

4.  Check the status of the cups services. Since when was it running?

It was running 6 minutes ago

SS:

![](vertopal_808139c8243f45408815596a49e28422/media/image6.png){width="7.027083333333334in"
height="3.25in"}

5.  Stop cups services.

6.  Verify if the service was stopped.

> ![](vertopal_808139c8243f45408815596a49e28422/media/image7.png){width="7.027083333333334in"
> height="3.748611111111111in"}

7.  Restart the cups services

8.  Verify if the service was restarted.

![](vertopal_808139c8243f45408815596a49e28422/media/image8.png){width="7.027083333333334in"
height="2.604861111111111in"}
