Assemble is a function that takes in data about a collection of notes and from those notes creates a javascript object that follows the midifile library format. The output object should be able to be directly converted into a midi file by the library.

First, we create a new midiFile object. This object will be the one returned by the function. Then we set what type of MIDI file the object is supposed to represent. Then we set the time division (or ticks per beat) for the song.

Second, we create a meta track (track zero) with the meta information necessary for the song. We create an array of events, add a time signature event, and a tempo event. We finally add an end-of-track event to the array and make it the track’s events.

Third, we add the actual instrumental tracks. We start a loop for each track.
    For each track,
        We create a new track in the output object.
        We grab the notes from our input variable.
        We set the track’s key signature.
        We loop through the array of notes we have:
        For each note,
            We add the delta time of the note to our overall tick count.
            If the note is a different instrument from the one currently selected, we insert an”instrument-change” event into the array of track events.
            We create the “note on” event and mark what tick this occurs at.
            Insert the event into the array of track events.
            We create the “note off” event and mark what tick this occurs at.
            Insert the event into the array of track events.
        We loop through our ticks that we marked, and for each tick:
            We note what events happen at that tick and give each event an appropriate delta time (time since the last event).
        Finally we add an end-of-track event to the array of track events.
        We set the track events to the array of events we just created.

When done, return the midiFile object.
