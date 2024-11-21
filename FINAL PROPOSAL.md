FINAL PROPOSAL

I think it would be very cool to manipulare pictures with OSC messages coming from PD. In PD I would also like to create a sampler that would be randomized by bangs that are linked to an metronome. I think that I could maybe take the data from the randomized bangs, and have them influence the visualizer. As of right now my main focus will be to create a good sampler inside of PD, and hopefully it will give me a strong start to the rest of the project. 


IDEAL PHASES


1. Get Samples to load automatically

2. Create a convinent sequencer which played said samples

3. Have each audio sample bang at the same time as a midi message, so that I can control Openframeworks 
with Midi messages, rather than figuring out controling things via audio spectrum. I feel that this could
give me more control over my visuals hypothetically speaking,, maybe>>>?? lol

4. OPTIONAL // If I have enough time on my end maybe during the openframworks phase of the project I can
figure out how to control the visuals via midi bangs from Pure Data, and via midi messages. 


PHASE 1: Getting Samples to load automatically.

Most of my patch is going to implement the Array functions to call for audio files 
with the "open pannel object, and the sound filler object. My current patch currently plays audio
files, but when I close the patch and re-open it I need to manually reload the samples into the patch.
This is very fustrating and I need to find a way for the samples to automatically load when I open the
patch before I move on to creating my sequencer 

-- I encounter this problem where I try to open an audiofile straight from my dirrectory and pure data cannot find it. Since calling for an audio file with the open panel object works, I used to print
object to copy the file directly from the log. This didnt work. I feel like this problem hopefully 
will be my biggest roadblock, so Im hoping to get it figured out soon. 

--I DID IT (it was a spacing error hahahahaajahahha) 

Here is the forum that helped me figure out my issue: https://forum.pdpatchrepo.info/topic/5915/finding-sound-files/4



PHASE 2: 

Now that my main issue is resolved, I am going to make a simple sequencer based off of the demo
sampler that you gave us in class, except instead of sending messages to ableton, this one 
will play audio files through PD, and send midi out. 

First I am going to create the sample playing portion of the sequencer. 

Before I begin anything, I am going to slice an amen break in ableton, export the files, and then create
a randomized sequencer in PD to give me interesting rhythms. 

The randomized sampler is very simple. Its Just a metro banging a ramdom  object, into a select object,
into a new bang which goes into tabplay object. The tabplay object is then calling from the buffer bassed off of the name after the ~ 

PHASE 3:

Getting the midi to send was extremely simple. I just took each bang that was connected to a sample, 
and then connected it to a number, which would then be fed into a makenote and noteout. 

I could not get IAC to work with ableton, so I guess  I will be partially working in logic for this project. 