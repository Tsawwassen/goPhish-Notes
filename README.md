# goPhish-Notes ( https://52.229.114.219:3333/ )
* currently have the campaign is able to
  * sending an email
  * tracking when the email is opened* (the email click template doesnt seem to track when the email is opened, but the previous version does. Need to look into that)
  * Send users to a landing page looking for username and password, then redirects when user clicks submit (password is currently turned off, don't want to keep that on but it does work)
  * submitted data is viewable on the dashboard
 
* TODO
  * email is getting quarantined by microsoft
  * even tried a basic text email and it still got blocked (need to confirm tomorrow)
  * Checked the header in chrome, and it looks much nicer then the MS one
    *  The 'From" header shows 'Zuper <zuper.create@gmail.com> Using gophish'...
    *  don't have a 'Reply-To: john.doe@example.com' header
    *  the 'Message-ID' is <1733280058127825077.4695.2989063290088956566@gophishTest> not <1234567890@mail.example.com>
    *  'X-Mailer: gophish' but should be X-Mailer: Microsoft Outlook 16.0 (?)
    *  don't have 'X-Originating-IP: [192.0.2.1]'
    *  return path has '<>' but example doesnt?
    *  missing 'X-Priority: 3 (Normal)'
    
 
   
* DONE
  * Need to find a way to keep the server running after powerShell is closed
    * used instructions found ( https://tzusec.com/tag/tzusec/ )
      * WorkingDirectory=/home/azureuser/gophish/gophish-v0.12.0-linux-64bit/
      * ExecStart=/home/azureuser/gophish/gophish-v0.12.0-linux-64bit/gophish
  * When adding an email to the 'Sending Profile' in goPhish, the password would be a 3rd party / single App password
    * Wasn;t that easy to find for gmail. eventually found a link to it on some randome forum
  * The pages/email received some TLC(SS).
  * Have full campaign work flow that sends a MS reset email, sends you to a MS reset page, captures user submitted data, redirects to MS page on submit
  * Get an idea of what company we would want to get people to spoof, make the page from that using the currecnt template files, adn what email will send it.
    * using zuper
 * Need a better email to send the phishing from.
    * created qa dummy gmail zuper aggou
    *
---------------------------------------------------------- 
------------------
--- keeping the server running---
-------------------

'nohup sudo ./gophish & '

