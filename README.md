#### CPSC 416 Capstone Project  
##### Instructions to Run on OSX:  

```
# Install dependancies
$ brew install sdl sdl_ttf sdl_gfx sdl_image sdl_mixer

# Build
$ make

# Run it
$ ./run
```

##### Name: Aaron Mast
##### Email: amast@clemson.edu</h4>
##### Date: 04/23/2012
##### Proj No: 5

##### Description:
1. Incorporated AI
2. Incorporated a Menu

##### To change the XML file and the animation:  
* Sprite sources, destinations, speeds, number of them.  
* MultiFrameSprite delays between frame updates, number of them.  
* Change how long the explosions last  
* Change how far a missle will travel  
* Change the min and max speed of the player  
* Change the number of any of the sprites other than the player  
* Change all of the locations, player is the only one who takes an exact coordinate the rest of the sprites are randomly generated  
* Setup initial number of enemies  
* Setup player breathing room for the start  
* You can change almost anything through the xml  


**\*MAKE SURE THE INITIAL VELOCITY MATCHES UP WITH THE CORRECT ROW OF THE SPRITE**  
(the way mine are, usually negative velocity will correspond to row 1 and positive velocity will correspond to row 0)

##### The Specs that I implemented are: 
* Enemy Class - used composite pattern to wrap MultiFrameClass with enemy features in order for enemies to be any MultiFrame sub class  
* Menu Classes - your menu implimentation, but added a gravity parameter and a help section  

##### The Specs that I was unable to implement are:  
* NONE!!! ITS PERFECT!!!  

##### Extras:  
* All sprites are feverishly sweat blood and tears made by yours truly.  

##### Notes:  
* See help section inside my menu for detailed information  

Enemey AI = if the player is within the attack range and in front of the enemy then the enemy will increase X and Y velocity by the attack speed, the Y velocity will be set to 0 when it reaches a Y of within 20 of the player
this is to reduce jutter if you make it stop exactly on the player Y coord because the player will not be holding to a constant Y coordinate, once these conditions are no longer met the enemy resumes it's previous velocities from before it was tracking the player  


####Note for El Captain (Xcode 7.* Users), if you still getting a,  

```fatal error: 'SDL/SDL.h' file not found```

####error you may need to install Xcode command line tools  

```$ xcode-select --install```
