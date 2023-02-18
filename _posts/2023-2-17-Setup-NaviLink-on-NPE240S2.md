---
layout: post
title: Setup NaviLink on NPE240S2
description: I could not find it in the manual they included, so this is what I found online.
image: assets/images/pic06.jpg
tags: IT Documentation Fun HomeAssistant
---

First of all, allow me to provide the only picture known to mankind of where you plug it in. There is a youtube video where even the professional installer is confused and he does plug it into the proper spot. There are an awful lot of manuals explaining how not to install it on the NPE-240S2, they must have changed their interfaces often.

![My helpful screenshot](/assets/images/navi.png)

Oh, and here's [the actual manual](/assets/pdf/NPE-2_Installation_Manual_EN_210216.pdf) for the NPE-240S2, I think, or at least the one with this section about how to enable the NaviLink port. Page 88 holds the well kept secrets. Section 6 in the manual that came with mine is about installing vent pipes. But, basically you hold the left top 2 buttons (menu and back) for 3 seconds and then enter the passcode which is defaulted at 1234. Pick 3, Application Settings and option 1 lets you enable the NaviLink port.

Now, if you're like me and had been watching the port lights not turn on and trying to connect it to your wifi, NEVER imagining they would just leave the port disabled... you may be where I am at now.. up the creek. Somehow using their 1.x/5 star rated application, maybe the 10th try it actually added the darn thing to their webpage. However, all it does is say it isn't connected and to go hit the wifi button.

If you did not already disable your NaviLink app, then try to set it up! This is in the manual that came with it, but you hold the black button closest to the edge for 3 seconds and in the app click your wifi settings (button at bottom) and connect it to your 2.4ghz channel. It does not support 5ghz. Wait for it to connect and set the use this time permission or whatever you want, (literally doesn't matter since it asks every time). Then, from all the information you got from the blank page prior, you hit the back button to get back to their app. If you do it too soon it just says it can't connect.

If you use Home Assistant, check out this little project multiple people have thrown in on: [Code](https://github.com/nikshriv/hass_navien_water_heater) and then the [Issues](https://github.com/nikshriv/hass_navien_water_heater/issues) thread to check if there are any ongoing issues. Long story short, Someone pioneered this, Bryan (can maybe search issues for more info) took it to the next step and nikshriv converted it to a Home Assistant module, at least that is how I understood it. As I write this blogpost at least both of the last 2 people I mentioned are working to get it back up and running after an authentication change on Navi's end. This is probably good and maybe means it would be more secure, you don't want any terrorist hackers messing with your water temperatures!

I will post another update once the Home Assistant is working again and include a screenshot of that as well as link to that post from here.

Lastly, I don't mean to shame the Navien team. They are likely more of plumbers at heart trying to get things updated for the future. They probably outsourced their apps creation which got it a bad review score. It is clunky. Hell, it could just be one employee writing it all themselves. So, as a thank you to them for even bothering to enable us to get data, some suggestions for the app.

* Enable the NaviLink port by default or include a little tape tag on it that says disabled see the installers manual to enable. I know it says professional installers only, but the people buying this product know their way around computers and can plug the thing in.
* App: most important, allow users to delete the only device in the app. I now have this broken one that I can not delete.
* App: in the connection part, have a warning to be sure your Wifi is green and your connected port is blinking green. Include a warning that you must access the installer setup to enable the port.
* App: On the wifi setup, put a little info. 'Select the Navi wifi and after it is connected go back to get back to our application which will try to connect to your phone' or something along those lines.
* App: I'm guessing some of those negative feedbacks are from people that did not know to enable that port. It is not very clear. The app could use a bit of work, but I haven't even been able to get into my unit yet, so I'll have to contact support tomorrow if I don't figure it out.