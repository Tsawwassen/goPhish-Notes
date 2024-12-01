# goPhish-Notes ( https://52.229.114.219:3333/ )
* currently have the campaign is able to
  * sending an email
  * tracking when the email is opened* (the email click template doesnt seem to track when the email is opened, but the previous version does. Need to look into that)
  * Send users to a landing page looking for username and password, then redirects when user clicks submit (password is currently turned off, don't want to keep that on but it does work)
  * submitted data is viewable on the dashboard
 
* TODO
  * The pages/email need some TLC(SS).
  * Get an idea of what company we would want to get people to spoof, make the page from that using the currecnt template files, adn what email will send it.
    * if we use Microsoft, most people don't know their password anyway. I would expect them to email us asking for it, and we would hopefully ask them why they need it, we see the email, and should (in a real world scenario) tell them its a phishing email
      * maybe just do a click here to make new password type email / form 
    * if we use something from their personal life (like amazon) they might wonder why they got an email to their work account about their personal account
    * System 5? WindWard? BambooHR? Zuper?
    * 
   
* DONE
  * Need to find a way to keep the server running after powerShell is closed
    * used instructions found ( https://tzusec.com/tag/tzusec/ )
      * WorkingDirectory=/home/azureuser/gophish/gophish-v0.12.0-linux-64bit/
      * ExecStart=/home/azureuser/gophish/gophish-v0.12.0-linux-64bit/gophish
  * When adding an email to the 'Sending Profile' in goPhish, the password would be a 3rd party / single App password
    * Wasn;t that easy to find for gmail. eventually found a link to it on some randome forum 

