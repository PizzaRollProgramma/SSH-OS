
                                                      Electron-OS/SSH-OS Setup Guide for Raspberry Pi

                                                       
                                                              ** Make sure ssh is enabled **
                                                                
                                                                © Copyright 2017 Ehncore soft
                                                                
                       ============================================================================================================================
 


 1 |Put these files in two directories

    Directory 1: /ect/ssh

    Directory 2: /home/pi

    Directory 3: /ect

    // T E R M I N A L :

    (from /home/pi)

    1 | cd ..

    2 | cd ..

    3 | cd ect

    4 | cd ssh

    5 | sudo git clone http://www.github.com/PizzaRollProgramma/Electron-OS

    6 | cd ..
    
    7 | sudo git clone http://www.github.com/PizzaRollProgramma/Electron-OS

    8 | cd ..
   
    9 | cd home

    10| cd pi

    11| sudo git clone http://www.github.com/PizzaRollProgramma/Electron-OS

    //

2 |Go to the ssh directory and delete 2 files

    Delete: ssh_config

    Delete: sshd_config
  
    // T E R M I N A L :
    
    (from /home/pi)
   
    1 | cd ..

    2 | cd ..

    3 | cd ect

    4 | cd ssh

    5 | sudo rm ssh_config

    6 | sudo rm sshd_config
   
    //

3 |Replace the config files
   
   Move ssh_config back to ssh folder

   Move sshd_config back to ssh folder
   
   // T E R M I N A L :
    
    (from /home/pi)
   
    1 | cd ..

    2 | cd ..

    3 | cd ect

    4 | cd ssh

    5 | cd Electron-OS

    5 | sudo mv ssh_config ..

    6 | sudo mv sshd_config ..

    7 | cd ..
 
    8 | sudo rm -r Electron-OS
   
    //

4 | Replace motd file

    Delete file named motd in /ect/

    // T E R M I N A L :
    
    (from /home/pi)
   
    1 | cd ..

    2 | cd ..

    3 | cd ect

    4 | sudo rm motd

    5 | cd Electron-OS

    6 | sudo mv motd ..
   
    //

5 | Add banner file

    Move a file named banner from /Electron-OS to /ect

    // T E R M I N A L :
    
    (from /home/pi)
   
    1 | cd ..

    2 | cd ..

    3 | cd ect

    4 | cd Electron-OS

    5 | sudo mv banner ..
   
    //

6 | Rename Electron-OS folder in /home/pi

   Rename the Electron-OS folder to elec
 
   // T E R M I N A L :

   (from /home/pi)
   
    1 | sudo mv Electron-OS elec

   //

7 | Move the source code file
   
   Move the source code file named Electron-OS.cpp to the pi directory
 
   // T E R M I N A L :

   (from /home/pi/Electron-OS)
   
    1 | sudo mv Electron-OS.cpp ..

   //
8 | Install and compile the OS

 ** This step should take from 3 - 6 minutes to compile **

  Compile the source code with g++ and name the executable Electron-OS

  // T E R M I N A L :

   (from /home/pi)
   
    1 | g++ Electron-OS.cpp -o Electron-OS

   //

 ***  WAIT UNTIL TIS STEP IS DONE BEFORE MOVING ON ***

9 | Delete folder and source code

    Delete the elec folder and the Electron-OS.cpp file from /home/pi

  // T E R M I N A L :

   (from /home/pi)
   
    1 | sudo rm -r elec

    2 | sudo rm Electron-OS.cpp

  //

10 | Change password

    Change the unix password to "electron"

    // T E R M I N A L :

   (from /home/pi)
   
    1 | passwd

   //



                   ---------------==================    Once all these steps are done make sure your interface looks like this ==================--------------







 
             Welcome to the entry page
                   for the ssh OS
               _______________________
               |E l e c t r o n - O S|

      password =  electron


pi@192.168.1.168's password:

                  *Go fullscreen!*

                type: ./Electron-OS
                   to start up OS

              E L E C T R O N - O S login:

              username = guest

              password = guest



                           



                                                          


                                                                            © Copyright 2017 Ehncore soft
