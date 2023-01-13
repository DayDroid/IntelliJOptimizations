# Simple IntelliJ Optimizations Guide for Windows
A 3-Step and simple guide on optimizing your IntelliJ IDEA Experience (Faster startup times and general improvements)


[Note: This guide is for IntelliJ and may apply to other IDEs by JetBrains s.r.o. You can download them by clicking this hyperlink](https://www.jetbrains.com/products/)

Step 1. (No Splash)
======

First, we will begin by disabling the startup splash screen. This appears when you start the program and looks like this:

![IntelliJ-Splash](https://user-images.githubusercontent.com/85541291/212012017-f875d477-9319-426b-bf54-ff8d48fd5458.jpg)


Start by navigating to the horizontal menu bar and click on '__**Help**__' (Located on the upper top left of the application)

![image](https://user-images.githubusercontent.com/85541291/212019780-a15cdec9-2622-4fdb-9cf2-f541e459c3b3.png)

Then, navigate downwards until you see '**__Edit Custom VM Options__**' and click on it.

![Edit-Custom-VM-Options](https://user-images.githubusercontent.com/85541291/212166310-8fa2ccd2-20f9-48b5-b44b-a4663a7ae000.png)

After that, a new window should pop up. Add the following text in your vmoptions:

```
-Dnosplash=true
```

![IDEA-VMOPTIONS](https://user-images.githubusercontent.com/85541291/212189676-fa389ad8-b7cb-48a3-941e-bc4f86466e9f.png)


Save and Restart your IDE. After doing so, you should find that startup time has been noticeably reduced and the startup screen is now gone.

#### Note: If you find that this does not work, try editing the **idea64.exe.vmoptions** text file in one __or__ all of these directories (Also make sure you fix the directories):
```
C:\Program Files\JetBrains\IntelliJ IDEA {YOUR INTELLIJ IDEA VERSION HERE}\bin\idea64.exe.vmoptions
```
```
C:\Users\{YOUR USER FOLDER}\AppData\Roaming\JetBrains\{YOUR INTELLIJ IDEA VERSION HERE}
```

Step 2. Increasing Memory
======

To increase IntelliJ's memory allocation, navigate back to the horizontal menu bar and click on '__**Help**__'. This time however, click on  '__**Change Memory Settings**__' and change the number inside to a preferable value. Because I have 32gb of memory I have decided to use 4096mb (4gb) to allocate to IntelliJ.

#### Note: This relies on your system configuration.

I have found 2gbs to be noticeably slower than 4gbs. You shouldn't need more than 4gb allocated and if you don't have enough system memory you would want to choose a lower number. For example:

System Memory (In gb) | 4gb | 6gb | 8gb | 12gb |16gb | 24gb | 32gb | anything above 32
--- | --- | --- | --- |--- |--- |--- |--- |--- 
**MY** recommended setting to use (in mb)| 1024 | 2048 **OR** 3072 **OR** 4096 | 3072 **OR** 4096 | 3072 **OR** 4096 | 4096 | 4096 **OR ANYTHING ABOVE** | 4096 **OR ANYTHING ABOVE** | 4096 **OR ANYTHING ABOVE**

![Change-Memory-Allocation-Settings](https://user-images.githubusercontent.com/85541291/212190931-42520be0-eb8f-4a6e-9aa4-35889e0b6134.png)

You can use any of these numbers or any you'd like. After writing your number in the textfield, go ahead and click on
'__**Save and Restart**__'


Step 3. Disabling unused plugins that are unnecessary for your development cases.
======

After doing all these, go ahead and press the keybind:
```Ctrl+Alt+S``` 
Look for the category '__**Plugins**__'

![Plugins](https://user-images.githubusercontent.com/85541291/212193633-1cdb1717-7711-4162-ad74-58a4b25eaf12.PNG)

I have found that disabling plugins that you do not use greatly reduces loading times for IntelliJ and provides a much smoother experience and more responsive application. To do so, start by disabling anything that does not apply to your usage scenarios. Be sure to click  '__**Apply**__' then  '__**Ok**__' after disabling plugins. After doing so, IntelliJ will prompt you to restart. Once fully done, **__Restart__** the application. That is all this guide will cover. Be sure to share this with others if this helps 😊



