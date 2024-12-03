  -------------------------------------------------------------------- -------------------------- ---
  ![](media/image1.png){width="2.4in" height="0.5881944444444445in"}

  SCHOOL OF INFORMATION AND TECHNOLOGY

  NAME: MAGNO, RONNIE L.

  Section: IDC2
  -------------------------------------------------------------------- -------------------------- ---

SYSADM1 – Managing Services in Windows
======================================

Requirement: 
=============

-   A virtual machine running Linux and Windows OS

    **Services** are background processes that run independently of user
    interactions in Windows. They provide essential system functions,
    such as network connectivity, printing, and time synchronization.
    This lab will guide you through the process of managing services
    using the Services app.

Instructions:  {#instructions .ListParagraph}
==============

1.  Open the Start menu and search for "Services"

2.  Familiarize yourself with the columns, including Service Name,
    Display Name, Status, and Startup type.

3.  Right-click on a service and select "Start", "Stop", or "Restart".
    Fill out the table below

  **Status**   **Name of Service **        **Screenshot**
  ------------ --------------------------- ----------------------------------------------------------------------------------
  Start        File History Service        ![](media/image2.png){width="4.5in" height="2.90625in"}
                                           
  Stop         Themes                      ![](media/image3.png){width="4.395833333333333in" height="2.6051793525809273in"}
  Restart      System Event Notification   ![](media/image4.png){width="4.71875in" height="2.62961176727909in"}
  Pause        Workstation                 ![](media/image5.png){width="4.6625in" height="2.808373797025372in"}

1.  Select five network services, right-click to view its properties.
    Modify the startup setting to Manual.

> **SS**:

  Network Connected Devices Auto-Setup   ![](media/image6.png){width="2.3472222222222223in" height="2.7291666666666665in"}
  -------------------------------------- -----------------------------------------------------------------------------------
  Network Setup Service                  ![](media/image7.png){width="2.2395833333333335in" height="2.611111111111111in"}
  Network List Service                   ![](media/image8.png){width="2.1659722222222224in" height="2.51875in"}
  Network Connections                    ![](media/image9.png){width="2.5236111111111112in" height="2.8229166666666665in"}
  Network Store Interface Service        ![](media/image10.png){width="2.486111111111111in" height="2.8854166666666665in"}

1.  Explore the "General", "Recovery", and "Log On" tabs to understand
    additional service settings.

2.  Create a batch file that will be added as a new service later on.
    Refer to the batch file code below.

> ![](media/image11.png){width="4.7962959317585305in"
> height="2.0005489938757655in"}
>
> ![](media/image12.png){width="6.355053587051619in"
> height="0.625087489063867in"}

1.  Save the batch file in Z:\\lastname\_timer.bat

2.  Use the sc command to add timer.bat service in the command
    line interface.

> *sc create BatchTimerService binPath=
> "path\_to\_your\_batch\_file.bat" start= auto*
>
> *net start BatchTimerService*
>
> **Replace path\_to\_your\_batch\_file.bat with the actual path to your
> batch file.**
>
> ![](media/image13.png){width="7.027083333333334in" height="1.41875in"}

1.  Verify that BatchTimerService has been added to the services.

> **SS:** ![](media/image14.png){width="5.661313429571304in"
> height="4.125in"}

1.  **Testing the Service:** Now, if you open a new command prompt, you
    should see the timer countdown without requiring your interaction.
    Once the timer finishes, you'll see the "Timer finished!" message.

> **SS:**
>
> ![](media/image15.png){width="3.25in" height="3.3810476815398074in"}

**Rubric**

  **Criteria**                  **Excellent (10)**                                                                                                 **Good (7)**                                                                               **Needs Improvement (3)**                                                          **Unsatisfactory (1)**
  ----------------------------- ------------------------------------------------------------------------------------------------------------------ ------------------------------------------------------------------------------------------ ---------------------------------------------------------------------------------- -----------------------------------------------------------
  Understanding of Services     Demonstrates a deep understanding of the concept of services, their roles, and their importance in Windows.        Shows a solid understanding of services, but may lack some depth in specific areas.        Has a basic understanding of services, but may struggle with specific concepts.    Shows little or no understanding of services.
  Service Management Skills     Successfully starts, stops, restarts, and configures services using the Services app.                              Demonstrates proficiency in managing services, but may encounter minor difficulties.       Can perform basic service management tasks, but may need assistance or guidance.   Struggles to perform even basic service management tasks.
  Custom Service Creation       Successfully creates and manages a custom service using the appropriate tools and techniques.                      Can create a custom service, but may encounter minor difficulties or require assistance.   Has limited experience with creating custom services.                              Cannot create a custom service.
  Problem-Solving               Demonstrates strong problem-solving skills when encountering challenges or errors.                                 Can effectively troubleshoot and resolve most issues related to service management.        May require assistance to troubleshoot some issues.                                Struggles to troubleshoot and resolve issues.
  Documentation and Reporting   Provides clear and concise documentation of the lab activities, including relevant screenshots and observations.   Documents the lab activities adequately, but may lack some detail or clarity.              Provides basic documentation, but may be disorganized or incomplete.               Does not provide any documentation or reporting.
  **Score:**                    **/50**
