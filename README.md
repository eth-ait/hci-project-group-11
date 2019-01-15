<p align="left" width="100%">
  <img style="width:30%;align:left" src="https://ait.ethz.ch/img/logo-ait.png"> 
</p>

# Sense Users' Musical Mood, Group 11
#### Nathaniel, Florian, Alexandre, Livio, Timon

## Project description
Teufel is a German company focused on providing their clients with excitement in form of music. They offer a big variety of speakers and headsets with all of them focusing on intensity and emotions.

Everybody listens to music! The goal is to bring the music system a step further and allow a more dynamic and automated music experience to the user. Instead of constantly having to search through playlists to find a good song to play the user should be provided with music whenever and wherever he is. We are looking for more ways to make music more enjoyable.

## Ideas

### Requirements
- Be able to find/discover/select the next song easily
- Create a seamless music experience across multiple devices/speakers
- Reduce interaction time needed to control music devices (improve on user experience of plug in earphones/turn on home speaker, pulling out smartphone, unlock phone, open Spotify, start play button)
- No need for extra hardware to carry with (using native speaker hardware or phone)


### Personas

Who are the users?
We came up with three interest groups and a concrete samples of a person that fits the given lifestyles.

#### Peter, 62
<img align="left" width="80" height="80" src="img/persona_peter.png">
Senior System Administrator: misses the good old days of radio. Listens to a lot of music but he always gets interrupted by colleagues. Stressful job, wants to put on headphones and then just have some music going. Doesn’t want to be bothered getting out the phone all the time just to adjust the music.


#### John, 28
<img align="left" width="65" height="80" src="img/persona_john.png">
Construction worker: Casually listens to music. But if he feels like he needs some music, he just wants to put on headphones and have some good music started. Doesn’t want to search ages for some music track he could listen to right now. Most of the time he just listens to the weekly discovery in spotify since he doesn't has any extensive playlists.


#### Courtney, 21
<img align="left" width="80" height="80" src="img/persona_courtney.png">
Instagram Influencer: Plans out all details of her life and takes pictures of everything. Takes public transportation to move between photo shoots, cafe hopping and bringing her dog on walks. Has tons of playlists and songs saved for each given task. Listens to her specific songs given what she is doing right now and how she is feeling. She has different playlists for doing yoga, go running, studying, hanging out with friends and going to bed but also for when she feels sad, lonely or when she is happy and excited.

### Affinity Clusters

<img align="width:30%;align:left" src="img/affinityclusters_overview.jpeg">

#### Software Features
- Artifical Intelligence
- Voice Control (Alexa, Siri, ...)
- Extension to existing Raumfeld App

#### Teufel Brand
- Do it different
- Niche products
- Experimental & crazy stuff
- Fans as customers
- Direct resell to customers

#### Music Experience
- Make music more enjoyable
- Boost emotions
- Improve music selection
- Support current ambience
- Suggest songs
- Reduce burden of searching for music 

#### Hardware
- Mood Button
- Lightning Sensor
- Microphone

#### Moods/Emotions/Experience
- Intense, cool, fun
- Loud
- Exciting

### Key Ideas
Out of over 50 ideas we generated the following two key areas

#### Seamless hardware-software integration
First of all, we want to achieve a fuss free transition between devices. If you leave the house you should have to press a minimum amount of buttons to keep the music playing on your headphones which was previously playing on the speaker. Preferably those transitions are hands-free. We could even take advantage of Smart Home integration. We also want to provide continuity by having the music play where you left the last time. Were you in the middle of an awesome playlist? It will continue playing when you put your headphones back on!  
Additionally we want to achieve a radio effect by allowing multiple people listening to the same music together. Potentially even across large distances. The music played should be automatically determined using common music preferences.

#### Data-driven music
Secondly, we need to understand our users through phone and sensor data such as location (GPS), date/time, seasons/holidays, local weather, calendar acvitities, activity and health data. Additionally we want to try understand our user through social media that could help us determine their overall mood and music preferences. This includes listening patterns on streaming services and understanding the user's habits such as how often music is played and what type of music according to a given context.  
Using sensors in the phone such as the microphone and acceleration sensor we can additionally reveal more information about the mood the user currently is in.

### Initial project ideas

Given Teufel's position as a audio hardware audio company, we thought it was ideal that Teufel brought value to the market in terms of combining sensor data (microphones, GPS location, weather, time of day etc.) with user data (eg. music listening habits and social media profiles) to make the music listening experience even more hassle-free for Teufel users. 

Our shortlist of ideas were as follows:

1. The Big Teufel Button
A Surprise me button that features easy-to use instant-music. 

2. Blast to the Past
Reminder of music you liked to play to boost your mood. Map locations to music to bring you back on a mind trip through old times.

3. Social Music
Use information from the environment (volume, amout of people, devices nearby) to select according playlists to match the mood of all guests.

See [our presentation](Deliverables/presentation_ideas_10_18.pdf) for the detailed write-up.

### Feedback from Stakeholder
After a discussion with our stakeholder we came to the following conclusion:  

The Big Teufel Button is a very good idea isn't as strong as the other's as you are quite limited in the amount of options you have to go from there. Blast to the Past is the most emotional option, which is always a big Factor for Teufel, but our Social Music idea had the most potential for Teufel overall.  

Therefore, we agreed to proceed with a focus of a social feature and the usage of sensors to detect, display and adjust a user's mood and integrate it into his music lifestyle. We therefore built a prototype based on the existing the value proposition Raumfeld mobile app that didn't focus on hardware sensors themselves but also .

## Prototyping

### First draft

<img align="left" width="200" src="img/idea_scheduler.jpg">

<img align="left" width="200" src="img/idea_moodgrid.jpg">

<img align="left" width="200" src="img/idea_moodselection.jpg">

<img align="left" width="202" src="img/idea_sensors.jpg">

<img align="left" width="202" src="img/idea_socialmusic.jpg">

   
During prototyping we focussed on the potential features and user interfaces for Teufel's Raumfeld app.
The goal is to provide an interface to the user to display his current (automatically detected) mood in a readable format and give the user the possbility to adjust it accordingly.
To represent the mood, we had to first find the right keyword (attributes) that both accurately describe a given mood state and that are understandable to the general user.

Furthermore there are multiple ways to present these settings as an interface for the user. For analogy, we looked at the screen brightness settings on a smartphone. The inital brightness is detected by the system but the user can still easily interact with a slider to adjust the brightness according to his/her liking.

The first option is to dislay each factor seperately using one-dimensional sliders. This way the user can specifically adjust each factor separately but in return might be overwhelmed by the amount of options.
![](img/interface2/Folie5.png)

The second interface uses a navigator in a 2-dimensional grid that can freely be moved around. Depending on where on the grid we find ourself, the chosen factors on the axis are taken into consideration according to the distance to the center of the grid. This allows for a very fast and easy adjustment but losing out on the option of fine-tuning each factor itself. There is also an option to gradually move the slider to the next position to achieve a smooth "mood transition".
![](img/interface2/Folie7.png)

In addition, we want to implement a social feature where the mood state of multiple present people are taken into account to create and/or adjust a playlist that is currently played. By extending Teufel's Raumfeld music app and the current mood of the user, the user can perform a gesture with his phone towards a Teufel speaker which then takes the user's mood into account. The Raumfeld app will be able to combined data from all the connected user's preferences, analyze signals from the ambient environment, and generate a music playlist of  that matches the general mood of the room.

![](img/social_feature.png)
    
## Evaluation

We conducted two complementary but separate user studies to evaluate the effectiveness of our user-interface ideas in helping music listeners to achieve their goals of finding the right music for them.

### First User Study

In a first iteration we want to find out what factors are used best to help identify a user's mood and how to assign those factors to a given song.

To do so we set up a survey that first asks the user to select factors which the user associates most with mood. This will help us determine which factors we should use on the interface.

The second task provided to our respondents requires the user listen to three different songs, and then rate out of 10 for each given music attribute how much they think that the song can be described by the attrivutre. For example, a classic piece from Mozart is expected to have a low "dancability" factor.

After reading the musical and scientific literature on mood classification (see example [1]), the attribute words we chose to evaluate were: 
- loudness: how loud the track is
- happiness: tracks that are positivity, cheerfulness, euphoric
- speechiness: presence of spoken words in the track
- tempo: beats per minute
- energy: intensity and activity
- danceability: suitability for dancing

We conducted a survey asking users to rate 3 songs based on these attributes. The results were as follows:

![](img/survey_avg.png?s=300)
![](img/survey_stddev.png?s=300)

We then compared the attribute values that were estimated according to Spotify's public API. After triangulating the error for each attribute we got the following results:
![](img/survey_error.png?s=300)

Based on the results of the initial survey, it was not clear if there was a subset of distinguishing characteristics that users would likely be able to . There was a wide spread in opinion amongst respondents. However in terms of accuracy (compared with the Spotify-generated feature values), loudness, energy and happiness topped the list in being consistent compared to user's understandings of the attribute words.

Since those results were not giving us more progress towards a more refined prototype we decided to conduct a second survey that is focused more on a concrete instance of one of our prototype. 

### Second User Study

In our second study, we chose to evaluate the effectiveness of a 2-dimensional touch interface in guiding the users to choosing the type of music that they wish to listen to. This was evaluated using music from 4 different genres (mainstream pop, rock, hip-hop/rap and instrumental). 

Respondents were asked to rate the attributes of the music they listened to on a 2-dimensional scale. We used randomization within-subjects to reduce the likelihood of ordering skewing the results in the favor of the later-presented items (to account for respondents getting more skilled at classifying music with each iteration). 

A converse case was then presented in which respondents were given a specific quadarant in a 2-dimensional attribute scale, and asked to think of a specific song in that quadrant. A reference song (generated by the Spotify public API) was then presented to them, and users were asked to rate how similar the reference song was to the one that they thought of.

The findings of the survey indicated that users are extremely divided on their opinions about the attributes of the music and are not always satisfied with the attirbutes and ratings that are automatically generated by servies like the Spotify public API. This made sense because individual music tastes tend to be subjective and widely varying.

To read more about the studies conducted, please read the the Study Report which provides full details including information about the data collected.


### Study Report

The lessons learnt from this exercise in conducting our studies indicated that that 

Please follow the link to read our full study including results: [Study Report (pdf)](Deliverables/study_report_group_11.pdf)   

### Feedback from Stakeholder

After presenting our results to Viktor from Teufel, our stakeholder, it was decided that we should put algorithms details aside since it is a very complex area and unfortunately out of scope for the course project. Instead more focus was to be placed on designing concept user interface that already assumes a backend sensor and database suite that is able provide accurate music prediction and mood detection services.

Upon discussion the user interfaces that our team had been exploring, Viktor and the team agreed that the 2-Dimensional Navigator is a fast and intuitive interface for users who simply want to choose a mood quickly. However, it might not be sufficient as a standalone interface. For example, an advanced user like Courtney may wish to tweak more than two attributes to get a specific playlist vibe that she wants. Viktor therefore agreed that we the team should explore supporting an "advanced option" for users that want to adjust their mood/music setting in more detail. This can be achieved, for example, through our 1-dimensional Slider prototype and additional drop-down menu to select specific genres.

## Approaching the final solution: an elegant user interface for mood listeners

With the outcome of the discussions with Viktor and the Teufel team in mind that we shifted our focus from exploring sensors and mood classification to developing a responsive and elegant user interface for music listeners.

We assume the availability mood data, ie. the user has provided sufficient training input about their music tastes and made available environmental sensors such that the mood of the user(s) can be predicted with reasobale accuracy. 

How can Teufel's mobile app Raumfeld be improved to accomodate interactivity with such features?

## Final Product

There are two key elements to our final product, Mood Mode (inpisre dby users like Peter) and Social Mode (inspired by users like Courtney). These are novel ways of listening to music that are designed to inspire, delight and surprise users with new music that suits the very mood that they are in, without having to press more than a few buttons to get started.

### Mood Mode

![Folie3](img/interface2/Folie3.png)
![Folie5](img/interface2/Folie5.png)
![Folie7](img/interface2/Folie7.png)

- Easily display and modify the user's current mood using the 2-dimensional Navigator interface. You can even enable a transition between two states in the Navigator such that the music adjusts over time from one mood setting to the other!

- The music instantly changes when the user scrubs from one position on the Navigator to the other, giving instant feedback to the user in a closed-feedback loop. This is important as users' music tastes are subjective and closed-loop feedback will be essential in giving users a sense of responsiveness to their mood adjustments.

- If a user wishes to go into pro-mode, they can use the advanced tab which features Slider interfaces for each attribute. This allows a precise definition of the genre you are looking for and the corresponding mood attributes. This way you can restrict the potential music results much better and an improved satisfaction with the music provided by our system will be achieved.

- Depending on where a user is and how many people are around them (using ambient volume as a proxy, for example), the attributes in the mood setting may change dynamically. If you are on a party with a lot of people, the attributes will include keywords such as dancability while on a relaxed walk in the park attributes such as ambiance will take over as the prevalent setting. This feature can be disabled by the user if desired.

### Social Mode

![Folie9](img/interface2/Folie9.png)
![Folie11](img/interface2/Folie11.png)
![Folie12](img/interface2/Folie12.png)

- If you meet up with other people or host social events often, use our Social feature! Mix your current mood and preferences with the other tch-savvy users around you. Based on the group's combined mood setting the music will adjust accordingly and provide you with a good sound for everyone's pleasure. Hosts can also provide a manual mood choice to override the autmatically generated mood.

- Guests can still directly influence what music is played using a song request feature - this way guests can help your host create a playlist by providing suggestions on potential songs that fit in with the current mood. This is also great for casual deejays who want to handle song requests on the fly. Hosts can still choose to manually accept or reject song requests through a veto setting in the app, if desired.

- Users can bring in their own mood to an ongoing playlist that is powered by Raumfeld by connecting their phone to a Teufel speaker. The new user's default mood settings and music preferences will be shared with the host's system and a new overall mood playlist will be generated.

- Savvy users of Teufel will no longer need to spend time haggling over what playlist to play on which phone - it will be as simple as connecting one's phone to the host speaker and Social Mode will instantly generate a mood that suits everyone's tastes. Finally, adding song suggestions has never been easier, just queue it up and enjoy the music!

## Final Video
You can find [our Video here](Deliverables/video_final_group_11.mp4).

## Comments; in closing
Our team (Group 11) is happy to have worked with Viktor and others at Teufel and were inspired by their vision ofmaking music even easier to listen to, for everyone. The journey was fulfilling and inspiring for us as we had hoped, and the learning process is just as valuable as if not more so than the product that we have designed. Many thanks to David and 
## References
[1] https://sites.tufts.edu/eeseniordesignhandbook/2015/music-mood-classification/
