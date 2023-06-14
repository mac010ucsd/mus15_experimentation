# Messing Around with MusicLM
## Project Concept:
Professor Lulu, in week 6 or 7, introduced "MusicLM", an online project hosted by Google's AI Test Kitchen. This AI tool works as follows: the user inputs a music-related prompt, to which the tool responds with two short AI generated audio snippets. Users will then listen to both audio snippets and vote on whichever track is "better".

My project will be to experiment with MusicLM. I think the output will be free-form of sorts: I will likely write a short analysis/guide on how to use MusicLM effectively, display some prompts/outputs I found interesting, and maybe take an audio clip and further develop it on my own.

## Overview
To use MusicLM, the user must first be registered to its public test via Google’s AI Test Kitchen. This requires the user to submit a brief application, which is then reviewed and then approved a few days later. Once the user has access to the webpage, they are greeted with a simple text box and output design. 

The user can type their prompt into the textbox on the left, and press enter to submit their prompt to the model. The model will then output two 20-second audio files on the right, which automatically start playing. After having listened to the two audio files, the user is prompted to give a “trophy” to whichever one is better. The user may download the audio file to their computer. The audio file is exported with the following properties:

| Thing       | Value                         |
|-------------|-------------------------------|
| Name        | audio/AI_Test_Kitchen_{prompts}.mp3 |
| Format      | MP3                           |
| Bitrate     | 128 kbps                      |
| Duration    | 19 seconds                    |
| File Size   | 310 KB                        |


In the file metadata, there is nothing that indicates that the file was AI generated, save for the title. The parameters for descriptions and artists are blank (not that metadata is a good way to determine copyright, as metadata is easily altered/changed).

## Prompting
### Basic Prompts
I decided to start with small inputs to see what would happen if specific descriptors were not given. I began with the most basic prompt, “music”, then moved on to basic genre descriptors and then full descriptions.

It turns out that MusicLM is not very good at making “music”. All of the audio files it generated were extremely disjointed; each one contained multiple different themes which changed as the song progressed. There were no transitions between the different themes, each one hard-cutting to the next one. It was as if someone had searched up “music”, picked multiple random songs, cut 2-5 second segments from each of them, and spliced them together. 

[music0](audio/AI_Test_Kitchen_music.mp3)

[music1](audio/AI_Test_Kitchen_music_1.mp3)

[music2](audio/AI_Test_Kitchen_music_2.mp3)

Genre descriptors were up next. I began with pop and then moved on to other (perhaps more niche) genres that I was more familiar with. Note: you don't need to listen to these to understand / continue reading, they're just kind of interesting and provide examples of what MusicLM produces.

[pop0](audio/AI_Test_Kitchen_pop_music.mp3)

[pop1](audio/AI_Test_Kitchen_pop_music_1.mp3)

[jazzfusion0](audio/AI_Test_Kitchen_jazz_fusion.mp3)

[jazzfusion1](audio/AI_Test_Kitchen_jazz_fusion_1.mp3)

[progrock0](audio/AI_Test_Kitchen_prog_rock.mp3)

[progrock1](audio/AI_Test_Kitchen_prog_rock_1.mp3)

Again, there isn't really a coherent idea throughout the song snippet. It's just a rough amalgamation of many different ideas that don't mesh well together. They also seem to not really capture the essence of the genre.

### Descriptors

What if we put in some descriptors? We should be more specific with the prompt so that the AI knows not to over-generalize and try to put too many topics in one. 

Prompt: ["pop music with guitars"](audio/AI_Test_Kitchen_pop_music_with_guitars.mp3). It's ok, at least the song itself shares the same theme or idea throughout. It feels like the guitars are being put in for the sake of putting them in. It starts with a clean guitar then suddenly distorts into an overdriven-toned guitar.

Prompt: ["pop music with a keyboard arpeggio and funky bassline"](audio/AI_Test_Kitchen_pop_music_with_a_keyboard_arpeggio_and_funky.mp3). This one's extra funky: seems like the addition of "funky bassline" really changes how the prompt is interpreted by MusicLM. I did try this prompt a few times and none of them had the "keyboard arpeggio" I specifically prompted for, though.

Prompt: ["pop music with powerful chords on the synth and an atmospheric feeling"](audio/AI_Test_Kitchen_pop_music_with_powerful_chords_on_the_synth_a.mp3). This one's interesting. It's very the weekend-esque which I wasn't really aiming for at the start but can see how the prompt leads the AI to generate such a song. Reverberating drums gives a very atmospheric feeling alongside the synth (not sure if that's because the song is theweekndified or if the AI is just good at it's job).

Notice that I've only been using "pop music" as the base genre descriptor so far. That's because I believe it has the largest sample size for this and it should represent the best of what the AI has to offer. What if I change it to a different genre?

Prompt: ["jazz music with a slow sax solo"](audio/AI_Test_Kitchen_jazz_music_with_a_slow_sax_solo.mp3). This was really unexpected. I thought it was going quite well for the first half, and then suddenly, BAM. Lofi/hiphop drum beat comes in with the sneaky genre change. I thought it was pretty slick. It did this for another song produced by the same prompt, too. I wonder if the rimshot sound of some slow jazz beats confuses the AI, making it associate it with the same sound in hiphop/lofi. 

Prompt: ["math rock with a joyous, upbeat feeling in odd time signatures"](audio/AI_Test_Kitchen_jazz_music_with_a_slow_sax_solo.mp3). It captured the joyous, upbeat feeling but did not really capture the essence of math rock. It felt more like somewhere inbetween normal rock and jazz fusion. It didn't really have the "odd time signature" that I was looking for, but I guess it did have like an extra beat somewhere in the middle to satisfy that requirement. The majority of the song had a standard time feel.

Short conclusion: It seems like the more specific you are with your prompt, the better it is. The less specific you are, the more generic it is (duh) and also the worse it sounds as it wants to grab multiple different parts of that genre and jam it into one song. It does pop significantly better than the other genres I have tried. It can portray specified emotions or "feelings" in the music depending on the prompt you give it. It's not good at more "technical" musical terminology (such as when I specified arpeggio, time signatures).

### Copying a Band
As noted before, artist names and band names have no effect on the output of the generation of the audio file. But what if we prompt using words which describe the style of the artist? 

I decided on experimenting on this using one of my favourite artists, Arch Echo (genre: progressive metal, fusion). Adjectives that come to the forefront of my mind are: “energetic, instrumental, fast-paced, harmonic, melodic”. Instrumental features involve “guitar runs, low tuned guitars, keyboard lines, powerful drums, fingerstyle bass”. I put all of the above into the prompts and hit the button:

[example1](audio/AI_Test_Kitchen_progressive_metal_and_jazz_fusion_with_an_ene_1.mp3)

[example2](audio/AI_Test_Kitchen_progressive_metal_and_jazz_fusion_with_an_ene.mp3)

It's bad. A lot of incoherent guitar wailing, not really melodic at all. The guitar gives off "classic metal shredding but we'll slow it down and make it really chromatic and have no sense of progression". The drums are maybe too strong, like I'm pretty sure I can hear a Michael Jackson type beat in the start of one of them, and it's definitely not in the style of either progressive metal or jazz fusion. The keyboard is lacking, I can't tell if it's not there or if they sound like really bad guitars. It doesn’t even sound like someone trying to imitate Arch Echo, but it’s the best I can do with the level of description permitted by MusicLM. I'm aware that from my experiments before that non-pop genres would be pretty bad, but I hoped that the extra precision in my prompt would make up for it. I tried working the prompt, changing/adding/removing keywords, but it didn’t get any closer to my ideal goal. As someone who isn’t a musical analyst, this is probably the best I could do on my own. However, there is a resource out there which has aggregated data from thousands of analysts around the world and could probably help: ChatGPT/Bing Chat.

### Using AI Tools
I find it kind of funny that I could be using AI to prompt another AI to do what I want. I decided to use Bing Chat as it is locally available in my browser and I don't need to fiddle that much to figure out how it works (Microsoft keeps pushing it to the user). I first tried asking it questions like, “What are the musical components of Arch Echo?” but ended up not getting results, or relatively unhelpful results like cutout phrases from the “About Me” section of their webpage. I then changed it to “Creative Mode” from “Balanced Mode”, and it began giving me results that were more useful. 

![image](Screenshot%202023-06-11%20185610.png)

[Example](audio/AI_Test_Kitchen_progressive_metal_fusion_with_influences_from.mp3). Honestly this isn't that great either, and with a bunch of tweaking and rewriting I still couldn't get it to sound any better. At least it's fusion-y? MusicLM seems to love putting a ton of chromatic notes whenever you include the word "metal" and I can't seem to get it to stop this habit (Arch Echo in general does not have a lot of chromatic notes). The phrasing is still very classic metal-esque.

I guess it does have all the elements of what I specified, just not implemented in the unique way that the particular artist does. Maybe the sample size is too small, or the artist is too rare, or whatever, but it did The Weeknd much better than it does Arch Echo, and that's just a limitation of the AI as is.

## Conclusion?
It was a pretty fun experience overall, coming up with prompts and then having some magic box spit out something that made music come out of these words. Even though it wasn't accurate most of the time for my prompts, admittedly it does do quite well when given a prompt that is pop-adjacent. It's really hard to try to verbally describe a song and a band's style exactly without likening it to another song/artist, and that provides a challenge in recreating another band's style in MusicLM.

TLDR: If you prompt using MusicLM, try to make it something about pop and use a lot of descriptors, especially those that invoke some kind of emotion. Everything you produce will be muffled.
