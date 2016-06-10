# MeetNow
An application for tracking meetings by using the ServiceNow platform.

This project was created during a 2 day hackathon run by ServiceNow at the University of Birmingham following
a 3 day course which was also run by the company. Four other students and myself worked
together over this time to produce the application. Our efforts earned us 2nd place out 18 groups.

The whole of the application is contained within the XML file in the repository as it is stored as an
'Update Set'. If you would like to use this application then in your ServiceNow instance, go to the filter
and under 'System Update Sets', select 'Retrieved Update Sets'. Then click on the link in the form called
'Import Update Set from XML'. From here you need to import the XML file that is found in this repository.
After that you then need to click 'Upload' and then access the record named 'MeetNowApp'. Click on the
button 'Preview Update Set' and then once it's finished previewing, click 'Commit Update Set'. You should
then be able to access the application by typing 'MeetNow' into the filter in the navigation pane.

Note that this is known to work for the Geneva release only. Compliance with newer or older releases
cannot be guaranteed.

The main feature of this meeting tracking system is that you can create 'Interactions'. These are be Meetings,
E-mail messages, Telephone calls and Conversations but others can be added if necessary. These interactions
are held by a host (who should have an entry in the sys_user table) with a client (who should have an
entry in the Client table - which is a table defined in the application). Searches can be made and reports 
viewed depending on whether you want to filter interactions by Meetings, E-mails etc. and also which rooms are
saved on the system. There is an integration with Google Maps which can be used to view where the actual meeting 
rooms are located. There are levels of access so standard 'host' users can request to make an interaction
of which a 'secretary' user must approve. Depending on the outcome of this approval, e-mail notifications
are sent to the host to inform them whether a booking was successful or not as well as whether one that
was already approved has been later cancelled. This is powered by ServiceNow's 'Workflow' system.
