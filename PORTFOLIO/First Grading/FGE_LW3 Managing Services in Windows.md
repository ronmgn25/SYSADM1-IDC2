![image](https://github.com/user-attachments/assets/fdf177df-5543-460e-b998-f0243477faf8)


# SYSADM1 -- Managing Services in Windows

# Requirement: 

-   A virtual machine running Linux and Windows OS

    **Services** are background processes that run independently of user
    interactions in Windows. They provide essential system functions,
    such as network connectivity, printing, and time synchronization.
    This lab will guide you through the process of managing services
    using the Services app.

# Instructions:  {#instructions .list-paragraph}

1.  Open the Start menu and search for \"Services\"

2.  Familiarize yourself with the columns, including Service Name,
    Display Name, Status, and Startup type.

3.  Right-click on a service and select \"Start\", \"Stop\", or
    \"Restart\". Fill out the table below

  --------------------------------------------------------------------------------------------------------------------------
  **Status**   **Name of      **Screenshot**
               Service**      
  ------------ -------------- ----------------------------------------------------------------------------------------------
  Start        File History   ![](vertopal_a6cd813a72774978bcde46cab32c6f83/media/image2.png){width="4.5381408573928255in"
               Service        height="2.9308825459317585in"}

                              

  Stop         Themes         ![](vertopal_a6cd813a72774978bcde46cab32c6f83/media/image3.png){width="4.465179352580927in"
                              height="2.6462773403324586in"}

  Restart      System Event   ![](vertopal_a6cd813a72774978bcde46cab32c6f83/media/image4.png){width="4.743001968503937in"
               Notification   height="2.6431266404199474in"}

  Pause        Workstation    ![](vertopal_a6cd813a72774978bcde46cab32c6f83/media/image5.png){width="4.730487751531059in"
                              height="2.8493252405949256in"}
  --------------------------------------------------------------------------------------------------------------------------

4.  Select five network services, right-click to view its properties.
    Modify the startup setting to Manual.

> **SS**:

  -------------------------------------------------------------------------------------------------------------
  Network        ![](vertopal_a6cd813a72774978bcde46cab32c6f83/media/image6.png){width="2.3472222222222223in"
  Connected      height="2.7291666666666665in"}
  Devices        
  Auto-Setup     
  -------------- ----------------------------------------------------------------------------------------------
  Network Setup  ![](vertopal_a6cd813a72774978bcde46cab32c6f83/media/image7.png){width="2.2395833333333335in"
  Service        height="2.611111111111111in"}

  Network List   ![](vertopal_a6cd813a72774978bcde46cab32c6f83/media/image8.png){width="2.1659722222222224in"
  Service        height="2.51875in"}

  Network        ![](vertopal_a6cd813a72774978bcde46cab32c6f83/media/image9.png){width="2.5236111111111112in"
  Connections    height="2.8229166666666665in"}

  Network Store  ![](vertopal_a6cd813a72774978bcde46cab32c6f83/media/image10.png){width="2.486111111111111in"
  Interface      height="2.8854166666666665in"}
  Service        
  -------------------------------------------------------------------------------------------------------------

5.  Explore the \"General\", \"Recovery\", and \"Log On\" tabs to
    understand additional service settings.

6.  Create a batch file that will be added as a new service later on.
    Refer to the batch file code below.

> ![](vertopal_a6cd813a72774978bcde46cab32c6f83/media/image11.png){width="4.808325678040245in"
> height="2.0055664916885387in"}
>
> ![](vertopal_a6cd813a72774978bcde46cab32c6f83/media/image12.png){width="6.355053587051619in"
> height="0.625087489063867in"}

7.  Save the batch file in Z:\\lastname_timer.bat

8.  Use the sc command to add timer.bat service in the command line
    interface.

> *sc create BatchTimerService binPath= \"path_to_your_batch_file.bat\"
> start= auto*
>
> *net start BatchTimerService*
>
> **Replace path_to_your_batch_file.bat with the actual path to your
> batch file.**
>
> ![](vertopal_a6cd813a72774978bcde46cab32c6f83/media/image13.png){width="7.027083333333334in"
> height="1.41875in"}

9.  Verify that BatchTimerService has been added to the services.

> **SS:**
> ![](vertopal_a6cd813a72774978bcde46cab32c6f83/media/image14.png){width="5.680470253718285in"
> height="4.138957786526684in"}

10. **Testing the Service:** Now, if you open a new command prompt, you
    should see the timer countdown without requiring your interaction.
    Once the timer finishes, you\'ll see the \"Timer finished!\"
    message.

> **SS:**
>
> ![](vertopal_a6cd813a72774978bcde46cab32c6f83/media/image15.png){width="3.25in"
> height="3.3810476815398074in"}

**Rubric**

  ---------------------------------------------------------------------------------------
  **Criteria**      **Excellent       **Good (7)**    **Needs          **Unsatisfactory
                    (10)**                            Improvement      (1)**
                                                      (3)**            
  ----------------- ----------------- --------------- ---------------- ------------------
  Understanding of  Demonstrates a    Shows a solid   Has a basic      Shows little or no
  Services          deep              understanding   understanding of understanding of
                    understanding of  of services,    services, but    services.
                    the concept of    but may lack    may struggle     
                    services, their   some depth in   with specific    
                    roles, and their  specific areas. concepts.        
                    importance in                                      
                    Windows.                                           

  Service           Successfully      Demonstrates    Can perform      Struggles to
  Management Skills starts, stops,    proficiency in  basic service    perform even basic
                    restarts, and     managing        management       service management
                    configures        services, but   tasks, but may   tasks.
                    services using    may encounter   need assistance  
                    the Services app. minor           or guidance.     
                                      difficulties.                    

  Custom Service    Successfully      Can create a    Has limited      Cannot create a
  Creation          creates and       custom service, experience with  custom service.
                    manages a custom  but may         creating custom  
                    service using the encounter minor services.        
                    appropriate tools difficulties or                  
                    and techniques.   require                          
                                      assistance.                      

  Problem-Solving   Demonstrates      Can effectively May require      Struggles to
                    strong            troubleshoot    assistance to    troubleshoot and
                    problem-solving   and resolve     troubleshoot     resolve issues.
                    skills when       most issues     some issues.     
                    encountering      related to                       
                    challenges or     service                          
                    errors.           management.                      

  Documentation and Provides clear    Documents the   Provides basic   Does not provide
  Reporting         and concise       lab activities  documentation,   any documentation
                    documentation of  adequately, but but may be       or reporting.
                    the lab           may lack some   disorganized or  
                    activities,       detail or       incomplete.      
                    including         clarity.                         
                    relevant                                           
                    screenshots and                                    
                    observations.                                      

  **Score:**        **/50**                                            
  ---------------------------------------------------------------------------------------