# Messing Around with MusicLM
## Project Concept:
Professor Lulu, in week 6 or 7, introduced "MusicLM", an online project hosted by Google's AI Test Kitchen. This AI tool works as follows: the user inputs a music-related prompt, to which the tool responds with two ~30 second AI generated audio snippets. Users will then listen to both audio snippets and vote on whichever track is "better".

My project will be to experiment with MusicLM. I think the output will be free-form of sorts: I will likely write a short analysis/guide on how to use MusicLM effectively, display some prompts/outputs I found interesting, and maybe take an audio clip and further develop it on my own.

## Overview
To use MusicLM, the user must first be registered to its public test via Google’s AI Test Kitchen. This requires the user to submit a brief application, which is then reviewed and then approved a few days later. Once the user has access to the webpage, they are greeted with a simple text box and output design. 

The user can type their prompt into the textbox on the left, and press enter to submit their prompt to the model. The model will then output two 20-second audio files on the right, which automatically start playing. After having listened to the two audio files, the user is prompted to give a “trophy” to whichever one is better. The user may download the audio file to their computer. The audio file is exported with the following properties:

Property
Value
Name
AI_Test_Kitchen_{prompts}.mp3
Format
MP3
Bitrate
128 kbps
Duration
19 seconds
File Size
310 KB 


In the file metadata, there is nothing that indicates that the file was AI generated. The parameters for descriptions and artists are blank (not that metadata is a good way to determine copyright, as metadata is easily altered/changed).
## Prompting
### Basic Prompts
I decided to start with small inputs to see what would happen if specific descriptors were not given. I began with the most basic prompt, “music”, then moved on to basic genre descriptors and then full descriptions.

It turns out that MusicLM is not very good at making “music”. All of the audio files it generated were extremely disjointed; each one contained multiple different themes which changed as the song progressed. There were no transitions between the different themes, each one hard-cutting to the next one. It was as if someone had searched up “music”, picked multiple random songs, cut 2-5 second segments from each of them, and spliced them together. 

[music0](/AI_Test_Kitchen_music.mp3)

[music1](/AI_Test_Kitchen_music%20(1).mp3)

[music2](/AI_Test_Kitchen_music%20(2).mp3)

Genre descriptors were up next. I began with pop and then moved on to other (perhaps more niche) genres that I was more familiar with. Note: you don't need to listen to these to understand / continue reading, they're just kind of interesting and provide examples of what MusicLM produces.

[pop0](/AI_Test_Kitchen_pop_music.mp3)

[pop1](/AI_Test_Kitchen_pop_music%20(1).mp3)

[jazzfusion0](/AI_Test_Kitchen_jazz_fusion.mp3)

[jazzfusion1](/AI_Test_Kitchen_jazz_fusion%20(1).mp3)

[progrock0](/AI_Test_Kitchen_prog_rock.mp3)

[progrock1](/AI_Test_Kitchen_prog_rock%20(1).mp3)

Again, there isn't really a coherent idea throughout the song snippet. It's just a rough amalgamation of many different ideas that don't mesh well together. They also seem to not really capture the essence of the genre.

### Descriptors


### Copying a Band
As noted before, artist names and band names have no effect on the output of the generation of the audio file. But what if we prompt using words which describe the style of the artist? 

I decided on experimenting on this using one of my favourite artists, Arch Echo (genre: progressive metal, fusion). Adjectives that come to the forefront of my mind are: “energetic, instrumental, fast-paced, harmonic, melodic”. Instrumental features involve “guitar runs, low tuned guitars, keyboard lines, powerful drums, fingerstyle bass”. I put all of the above into the prompts and hit the button:

It’s not great. It’s not Arch Echo. It doesn’t even sound like someone trying to imitate Arch Echo, but it’s the best I can do with the level of description permitted by MusicLM. I tried working the prompt, changing/adding/removing keywords, but it didn’t get any closer to my ideal goal. As someone who isn’t a musical analyst, this is probably the best I could do on my own. However, there is a resource out there which has aggregated data from thousands of analysts around the world and could probably help: ChatGPT/Bing Chat.

### Using AI Tools
I find it kind of funny that I could be using AI to prompt another AI to do what I want. I decided to use Bing Chat as it is locally available in my browser and I don't need to fiddle that much to figure out how it works (Microsoft keeps pushing it to the user). I first tried asking it questions like, “What are the musical components of Arch Echo?” but ended up not getting results, or relatively unhelpful results like cutout phrases from the “About Me” section of their webpage. I then changed it to “Creative Mode” from “Balanced Mode”, and it began giving me results that were more useful. 
