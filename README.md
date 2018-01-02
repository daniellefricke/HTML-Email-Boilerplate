README w/troubleshooting tips and tricks in progress!!!

#HTML EMAIL BOILERPLATE#

##PURPOSE:##
  I started this repo after changing jobs and being assigned emails. I quickly found that while coding them is circa 1998, email clients treat them differently. There are tons of email coding specific websites, forums, and Stack Overflow questions with great answers out there. I'm compiling this repo with the most useful fixes I've found. This also helps me keep track of them.

###HIGH LEVEL BEST PRACTICES:###
      - <table> instead of <div>
      - #FFFFFF instead of #FFF
      - padding not margin
      - CSS2 instead of CSS3
      - HTML4 instead of HTML5
      - background-color or bgcolor - not background
      - HTML attributes instead of CSS
      - Inline CSS instead of style sheets - Style in the head is needed too
      - Set a preheader text for emails that show preview text
          <span style="color: transparent; display: none !important; height: 0; max-height: 0; max-width: 0; opacity: 0; overflow: hidden; mso-hide: all; visibility: hidden; width: 0;">Preheader text goes here</span>



###EMAIL CLIENT BEST PRACTICES & FYIs:
    Gmail:
      - Recognizes inline css & media-queries (as of 2016)
      - CSS properties recognized by Gmail: https://developers.google.com/gmail/design/reference/supported_css
      - Non-standard fonts from Google Fonts can be used with a webkit  specific media query
              @import url(http://fonts.googleapis.com/css?family=Pacifico);
              @media screen and (-webkit-min-device-pixel-ratio:0) {
              }

    Outlook:
      - Conditionals can be used for MS specifics:
        <!--[if mso]>
          Only Microsoft Word-based versions of Outlook will see this.
        <![endif]-->
      - Outlook does not automatically render images

    Other:
      - GIFs are supported by most email clients. MSO 2007/2013 do not, but render the first frame of GIF.
      - Video is supported by iOS, AppleMail, and Outlook.com - https://www.emailonacid.com/blog/article/email-development/a_how_to_guide_to_embedding_html5_video_in_email/

###FIXES:
  Android/Email:
    Hairlines
    **FYI - Android/Gmail rounds up pixels when resizing table and rounds down pixels when resizing images.**
      1. Try shrinking images by a pixel or two.

  Outlook:
    Gap between images
       1. Add a line height to the cell that contains the image. Make it set to the same height as the image.

###RESOURCES:
Here are some of my favorite resources.
  If you're just starting with HTML emails, read this well-rounded overview of HTML email development: https://www.smashingmagazine.com/2017/01/introduction-building-sending-html-email-for-web-developers/

  1. Litmus: https://litmus.com/resources
  2. Campaign Monitor: https://www.campaignmonitor.com/
    - CSS Reference Guide! Know what css identifiers work in which email client! https://www.campaignmonitor.com/css/
  3. Email on Acid - Their forum has a lot of questions/answers: https://www.emailonacid.com/forum
  4. Stack Overflow - search this for previously answered questions :) or post a new one.
  5. Pretext previewer (IPad and IPhone) - https://codepen.io/awoodall/full/XbpMbo


###CONTRIBUTE!
If you have a fix or trick, please submit an issue/pull request - which ever makes more sense.
