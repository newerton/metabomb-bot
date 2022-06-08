<h1 align="center">

![Meta Bomb Banner](https://raw.githubusercontent.com/newerton/metabomb-bot/main/images/readme/banner.jpg)

  <a>
    💣 MetaBomb Bot 💣 
  </a>
</h1>

# MTB donation for bot development
![Timeline](https://progress-bar.dev/0/?title=10000%20MTB%20to%20Development)

Balance: https://bscscan.com/token/0x2bad52989afc714c653da8e5c47bf794a8f7b11d?a=0x4847C29561B6682154E25c334E12d156e19F613a

MTB: 0x4847C29561B6682154E25c334E12d156e19F613a  
PIX (Brazil): 08912d17-47a6-411e-b7ec-ef793203f836  

## ⚠️ Warning

I am not responsible for any penalties incurred by those who use the bot, use it at your own risk.

## 📌 Glossary

  * [Donation](#donation)
  * [How to works](#how-to-works)
  * [How config the bot](#how-config-bot)
    * [What are the problems](#what-are-problems)
    * [Threshold in config file](#threshold-config)
    * [Image replacement](#image-replacement)
    * [Some behaviors that may indicate a false positive or negative](#some-behaviors)


## 🎁 <a id="donation"></a>Donation
MTB: 0x4847C29561B6682154E25c334E12d156e19F613a  
PIX (Brazil): 08912d17-47a6-411e-b7ec-ef793203f836  

## ⚠️ <a id="how-to-works"></a>How to works?

The bot doesn't change any of the game's source code, it just takes a screenshot of the game's screen to find the buttons and simulates mouse movements.

## ⚠️ <a id="how-config-bot"></a>Adjusting the bot

**Why some adjustments might be necessary?**

The bot uses image recognition to make decisions and move the mouse and click in the right places.  
It accomplishes this by comparing an example image with a screenshot of the computer/laptop screen.  
This method is subject to inconsistencies due to differences in your screen resolution and how the game is rendered on your computer.  
It's likely that the bot doesn't work 100% on the first run, and you need to make some adjustments to the config file.

<a id="what-are-problems"></a>  

**What are the problems?**

* **False negative** - The bot was supposed to recognize an image, for example the push to work button, but it didn't recognize the image in the screenshot.

* **False Positive** - The bot thinks it has recognized the image it is looking for in a place where this image does not appear.

To solve these problems there are two possibilities, adjusting the "threshold" parameter in the config.yaml file or replacing the example image in the "targets" folder with one taken on your own computer:

  <a id="threshold-config"></a>
  ### **Threshold in config file**

The "threshold" parameter regulates how confident the bot needs to be to consider that it has found the image it is looking for.  
This value is from 0 to 1 (0% to 100%).  
Ex:  

A threshold of 0.1 is too low, it will assume that it has found the image it is looking for in places it is not showing (false positive). The most common behavior for this problem is the bot clicking random places around the screen.

A threshold of 0.99 or 1 is too high, it won't find the image it's looking for, even when it's showing up on the screen. The most common behavior is that it simply doesn't move the cursor anywhere, or crashes in the middle of a process such as login.

  <a id="image-replacement"></a>

  ### **Image Replacement**

  The example images are stored in the "images/themes/default" folder. These images were taken on my computer with a resolution of 1920x1080. To replace some image that is not being recognized properly, simply find the corresponding image in the folder "images/themes/default", take a screenshot of the same area and replace the previous image. It is important that the replacement has the same name, including the .png extension.

  <a id="some-behaviors"></a>

### **Some behaviors that may indicate a false positive or negative**

### False positive:

- Repeatedly sending a hero who is already working to work on a infinite loop.
   - False positive on "work_button.png" image, bot thinks it sees the dark button on a hero with the light button.

- Clicking random places (usually white) on the screen
   - False positive on image "metamask_sign_button.png"
 
 ### False negative:

- Not doing anything
  - Maybe the bot is having problems with its resolution and is not recognizing any of the images, try changing the browser setting to 100%.

- Not sending the heroes to work
  - It may be a false negative on the image "bar_green_stamina.png" if the option "heroes.mode" is set to "green".

## 👍 Did you like it? :)

### MTB: 0x4847C29561B6682154E25c334E12d156e19F613a  
### PIX (Brazil): 08912d17-47a6-411e-b7ec-ef793203f836