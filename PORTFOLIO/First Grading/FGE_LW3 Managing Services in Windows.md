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

![image](https://github.com/user-attachments/assets/7ee33de1-434f-4de3-acdf-7e46811fb489)
![image](https://github.com/user-attachments/assets/2a5c6d64-978d-492c-be39-c615090ed8d2)


4.  Select five network services, right-click to view its properties.
    Modify the startup setting to Manual.

> **SS**:

![image](https://github.com/user-attachments/assets/ed58aac1-269a-46ad-9c19-11250ff7d810)
![image](https://github.com/user-attachments/assets/5aa79d25-4605-4868-a175-b183697e6da0)


5.  Explore the \"General\", \"Recovery\", and \"Log On\" tabs to
    understand additional service settings.

6.  Create a batch file that will be added as a new service later on.
    Refer to the batch file code below.

![image](https://github.com/user-attachments/assets/4ac8e452-9cc1-4626-a4ed-087ca2c71464)


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
![image](https://github.com/user-attachments/assets/e0c0865b-f4b1-4c93-9334-25e471333c0b)


9.  Verify that BatchTimerService has been added to the services.

![image](https://github.com/user-attachments/assets/e56189d4-815e-4d71-9a47-366dde6c8c76)


10. **Testing the Service:** Now, if you open a new command prompt, you
    should see the timer countdown without requiring your interaction.
    Once the timer finishes, you\'ll see the \"Timer finished!\"
    message.

![image](https://github.com/user-attachments/assets/0d434207-5465-4e93-87ba-ee18d12eb4e2)


![image](https://github.com/user-attachments/assets/87c7d6e7-b4c3-46db-b8c3-eec8f3ae964e)

