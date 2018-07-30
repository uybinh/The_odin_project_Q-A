# Mailers

* What is a mailer?
  - to send email Rails use the ActionMailer gem

* How do you set up a new mailer from the command line?
  - `UserMailer.welcome_email`

* How are mailers similar to controllers? To models?
  - Mailer pretty much like controller and models `baked into one` and also have views

* How do you pass instance variables from the mailer to the mailer view?
  - Just like passing instance variables in controllers to views

* Why do you need both a text and HTML version of your mails?
  - When `HTML` is disable, you need the `text` version so that the emails can be view
  - Having two versions also helps bypassing spam filter

* How do you send an email directly from the Rails console?
  - for example with the `UserMailer` class `welcome_email` action
    ```
    UserMailer.welcome_email.deliver_now!
    #or
    UserMailer.welcome_email(@user).deliver_now!
    ```

* How can you take advantage of add-ons and third-party programs to send email?
  - We can use SendGrid. We don't have to do the config and settings behind the scene.

* What is the letter_opener gem good for?
  - We use this gem in `development` to prevent accidently send email to a real email address

* Why can’t you use *_path link helpers in mailer views?
  - Email clients have no web context and so paths have no base URL to form complete web addresses. Thus, you should always use the `_url` variant of named route helpers.

* How do you style up a pretty looking HTML email?
  - User `style` tag of user `inline style`