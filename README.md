# MCMF

MF (DTMF/MF4) dialling for the Psion MC400 - the Series 3 and later Psion machines had MF dialling capability built in but the MC-series laptops pre-dated those machines and missed out... until MCMF!
  
    
  files here uploaded from MCMF10.zip (http://cd.textfiles.com/psion/disk2/OTHER/SUNSITE/UTILS/MCMF10.ZIP) for archival

See https://bit.ly/MCMFopl

![MCMF in action on MC400](https://zedstarr.files.wordpress.com/2021/05/screen02a.png)

MCMF.TXT:
      
               ---- PSION MC-400 DTMF Dialler Utility v1.0 ----  Apr. '95
      
      This ZIP file should contain:
      
           MCMF.OPO    The OPL executable
           MCMF.ICN    An Icon for installing MCMF into System window
           MCMF.OPL    The OPL source
           MCMF.TXT    This File!
   
      This utility written by Chris Farrow.
      
      Credits
      -------
      
      The OPL implementation of "Bring" used  in this program is based on  code
      originally written in C by Colly Myers and translated to Series 3 OPL  by
      Tom Dolbilin, adapted for the MC with help from David Wood at Psion.
      
      Disclaimer
      ----------
      
      You are free to use and modify MCMF  and the OPL source as you wish,  but
      the author cannot be held responsible for any problems or data loss  that
      may arise, from use of this program, modified or otherwise. This  program
      has only been tested on an MC-400 (Word) V2.60F.
      
      MCMF v1.0
      ---------
      
      This utility has two modes of operation:
      
      (i)  Edit Mode:  The number to  be dialled is entered  and can be  edited
      before pressing  <Enter> which  will cause  any diallable  digits in  the
      input string to be dialled.
      
      (ii)  Free-form  Mode:  Any  diallable  digit  entered  will  be  dialled
      immediately.
      
      The following parameters are changeable, and  are stored in a setup  file
      (MCMF.DEF) when the program runs.
      
           Tone time
           Delay time
           Pause time
           Tone volume
      
      Also the current mode of the program is stored so that when next run,  it
      will start up in the mode it was last used in.
      
      It is possible to "bring" data into  the dialler (Edit mode only) in  the
      same way as the native MC apps. For example, find an entry in a  database
      file, highlight the no. you  want to dial, switch  to MCMF and bring  the
      number on to the input line.
      
      
      Running MCMF
      ------------
      
      To install  MCMF into  the system  window, copy  the files  MCMF.OPO  and
      MCMF.ICN to the same directory on a local MC disk. From the system window
      select "Install..." (Psion-V). Use  the file selctor  to navigate to  the
      directory where you put MCMF.OPO and select this file. The telephone icon
      should now appear in the system window.
      Whenever MCMF is run it will look for a file in the root directory of the
      default drive called "MCMF.DEF", which  contains default values for  tone
      time and delay  time etc.  If it  is not present,  MCMF will  ask you  to
      confirm or change the defaults, and then create the file.
      The settings are:
         Tone Time: The time the MF tone is actually present
         Delay Time: The time between the MF tones
         Pause Time: The time the "," charcater pauses for (see below)
         Tone Volume: The volume the tone is played at, Quiet, Medium or  Loud
      Once the defaults have been set up,  you will be presented with a  screen
      like this:
      
                 --- MC-400 DTMF Dialler ---
      
             Input No. to be dialled then <Enter>
      
        ("U <Enter>" changes defaults, "X <Enter>" exits)
       ("L <Enter>" brings data, "M <Enter>" changes mode)
      
       ->
      
      Any text entered  will appear by  the cursor ("->"),  the delete key  and
      cursor keys are available to move along  the input line and edit it.  The
      escape key  will clear  the contents  of the  input line.  The number  is
      dialled by pressing "Enter". Diallable characters are  "0123456789ABCD*#"
      and ",". The "," character is used  to insert a delay (the time of  which
      is alterable), for instance if dialling via a PABX, where a dial-out code
      is needed, followed by  a pause before a  second dialling tone is  heard.
      Any non-diallable characters are  ignored and stripped  out of the  input
      string, so it doesn't matter if you  ener a number as "0151 254 3000"  or
      "0151-254-3000". After dialling a number  the previous string remains  on
      the input  line, and  is  available for  re-editing or  re-dialling.  The
      "Escape" key clears the input line.
      Should you wish to alter the default tone times etc. then enter "u" on  a
      blank line (Case is not important), and MCMF will allow you to change the
      settings. Currently all times are in 1/24ths of a second and are  minimum
      1/24ths and maximum 99/24ths.
      In Free-form mode the digit entered is dialled instantly and displayed by
      the cursor.
      Entering "x"  on a  blank line  exits  the program  (again, case  is  not
      important).
      
      I have  had a  100%  success rate  using this  program  to dial  on  many
      different types  of  phone, I  have  found that  holding  the  microphone
      approx. 10cm over the MC speaker gives best results.
      
      
      Limitations
      -----------
      
      Firstly, me! I do not pretend  to be the world's greatest programmer  and
      although I have tried to make this program as resilient as possible there
      are bound to be  some situations I have  overlooked. The delay times  are
      implementend with the OPL command "pause"  and as such cannot be  exactly
      guaranteed by  the system,  so you  may notice  irregular pauses  between
      digits. This should  not cause  any problems  though as  the delays  will
      always be *longer* than specified.
      In Free-form mode, don't dial too quickly! The program cannot respond  to
      input as quickly  as you  can type  it. At  present only  the last  digit
      dialled is displayed - this may change in future versions.
      If the Link is running and active (i.e. you are transferring files)  then
      there will be some degradation in  the quality of the MF tones,  possibly
      to the extent that they may  not be recognised by the telephone  network.
      For this reason it  is wise not  to attempt to use  this program to  dial
      while there is lots of background activity on the system.
      
      Any  bug  reports   or  comments   welcome,  preferably   by  e-mail   to
      cxf@cix.compulink.XX.XX or failing that (as  a last resort only  please!)
      by phone to 01704 XXXXXX.
      
      Chris Farrow 3/4/95
