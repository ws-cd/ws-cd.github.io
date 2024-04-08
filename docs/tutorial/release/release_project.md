---
layout: en
title: Project Release
nav_order: 2
parent: Release
grand_parent: Developer's Guide
---

## Select modules to release
Click the project tool on the left navigation pane, click Release, select which modules to release, and then click Release Button. 
If there is an **update after publishing**, you need to click Release again to make the update take effect.

![project_release0.png](/assets/images/tutorial/release/project_release0.png)

## Releasing
As shown in the figure, after the module to be released is currently selected, an icon will prompt the task status on the left side of the release button, and the text of the release button will change to being released. At this time, users can jump to other pages to operate, or stay here to wait for the completion of training,
Or click Stop to stop releasing.

![project_release1.png](/assets/images/tutorial/release/project_release1.png)

## Releasing completed

As shown in the figure, after the releasing is completed, the icon next to the releasing will change, and the mouse will be placed on the icon to prompt the completion of the releasing.

![project_release2.png](/assets/images/tutorial/release/project_release2.png)

## Test
As shown in the figure, enter the chat information in the robot dialog window to verify whether the robot replies as expected.
What we verify here is that the user asks whether the fruit price can correctly obtain the fruit price information from the webhook, and the result meets the expectation.

![project_release3.png](/assets/images/tutorial/release/project_release3.png)

## Release in your app
The released project can be deployed through QR code and embedded any web pages

Requirement:
 - Internet support
 - Allow access: https://app.promptai.us  at port: 443
 - Modern browsers: like latest version of Chrome

###  QR code [Mobile]
When you need to access the mobile terminal, you can experience it by accessing the mobile terminal link or scanning the QR code.
![project_release4.png](/assets/images/tutorial/release/project_release4.png)

* Embed the QR code into the website, and users can experience the published projects through mobile browser scanning or WeChat scanning

<img src="/assets/images/tutorial/release/project_release6.jpg" alt="project_release6.png" width="390"/>

### Web page 
1. As shown, here we have prepared a project and released it in the project
   ![project_release5.png](/assets/images/tutorial/release/project_release5.png)

    - Paste the "Web Embedded Code(javascript)" in your html header
    ```html
        '<!DOCTYPE html>
        <html lang="en">
        <head>
          <meta charset="UTF-8">
          <meta http-equiv="X-UA-Compatible" content="IE=edge">
          <meta name="viewport" content="width=device-width, initial-scale=1.0">
          <title>Document</title>
          <style>
            * {
              margin: 0;
              padding: 0;
              box-sizing: border-box;
            }
            body {
              background-color: linen;
            }
            main {
              display: flex;
              justify-content: center;
              align-items: center;
              height: 100vh;
            }
          </style>
        </head>
        <body>
          <main>
            <h1>Your App...</h1>
          </main>
          {Your script is here.}      
        </body>
        </html>  '  
    ```

2. When we open the website, we can see that there are more chat boxes in the lower right corner of the website. Click Open to start an intelligent session. So far, our intelligent session has been published.
   ![release_web_script_demo_1.jpg](/assets/images/tutorial/release/project_release7.jpg)
