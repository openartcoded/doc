Once done, up the stack:

    docker-compose up -d


Open a private browser's window and visit [BackOffice](https://backoffice.somehost.org)

    default username: nordine
    default password: 1234

> If you get multiple warnings from your browser when opening the link, this is normal. Certificates are self-signed (only local)
### Expenses & Reminder Tasks features

Expenses management & reminder tasks use email to receive expenses from a known email address (in the case of expenses),
and send email in case of a reminder task. To test both features, follow these instructions:

- On the top-right  of `https://backoffice.somehost.org`, click on "Personal Info" then "Contact/Bank"
   and change the email address to `noreply@somehost.com`

- Open a new tab & Go to `https://mail.somehost.org` . You can login with `username: noreply@somehost.com , password: noreply`

- Send an email with an attachment (pdf or image) to `fee@somehost.com` => after a few seconds you should see a notification coming in on `https://backoffice.somehost.org`

- Create a new reminder task. Choose "Send Mail" . Once the task is triggered, go back to `https://mail.somehost.org` and login. 
  you should see an email with the reminder.