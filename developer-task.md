# Jiminny Developer Take Home Project

We recommend writing answers in whatever language you’re most comfortable in. Like our own code, we expect testing instructions: whether it’s an automated test framework, or simple manual steps.

You might find [gist.github.com](https://gist.github.com/) or [jsfiddle.net](https://jsfiddle.net/) a convenient way to send us your work.

---
There are tasks for both frontend and backend roles, each solving a real-life problem related to converting an audio file into a useful waveform. Waveforms are a key way for our customers to visualize speech data.

## Waveform Generator (Backend Task)

Write a program to consume the raw output from an audio silence detection [filter](https://ffmpeg.org/ffmpeg-filters.html#silencedetect) and convert it into a useful format.

The raw output contains data about a real conversation between two parties on a conference call. 

There is data for both the [`user` channel](https://rawgit.com/jiminny/join-the-team/master/assets/user-channel.txt), and the [`customer` channel](https://rawgit.com/jiminny/join-the-team/master/assets/customer-channel.txt). The data contains the following structure:

```
[silencedetect @ 0x7fa7edd0c160] silence_start: 1.84
[silencedetect @ 0x7fa7edd0c160] silence_end: 4.48 | silence_duration: 2.64
[silencedetect @ 0x7fa7edd0c160] silence_start: 26.928
```

1. For each channel, the data needs inverting to show when audio was active and stored as a series of points.
For example, the above would translate to `[0, 1.84], [4.48, 26.928]`

2. Determine the longest un-interrupted speech (monologue) for each channel.

3. Determine the percentage of time the user talked over the entire call duration.

You'll need to return the following JSON structure:

```
{
  "longest_user_monologue": 416.18,
  "longest_customer_monologue": 1152.82,
  "user_talk_percentage": 41.92,
  "user":[
    [0,3.504],[6.656,14],[19.712,20.144],[27.264,36.528],[41.728,47.28],[49.792,61.104],[65.024,79.024],
    [ ... and many more ...]
  ],
  "customer":[
    [0,1.84],[4.48,26.928],[29.184,29.36],[31.744,56.624],[58.624,66.992],[69.632,91.184],
    [ ... and many more ...]
  ]
}
```


## Waveform Visualizer (Frontend Task)

You'll start with a [JSON payload](https://rawgit.com/jiminny/join-the-team/master/assets/wavedata.json) from a real conference call.

Here you’ll interact with a REST API that returns information about a conversation between two parties.
The response payload contains a simple array structure, the `user` channel, and the `customer` channel.

Each channel contains an array of points that indicate when the audio channel was active (speech started), and when speech stopped (the order is important).
The data looks a bit like this:

```
{
  "user":[
    [0,3.504],[6.656,14],[19.712,20.144],[27.264,36.528],[41.728,47.28],[49.792,61.104],[65.024,79.024],
    [ ... and many more ...]
  ],
  "customer":[
    [0,1.84],[4.48,26.928],[29.184,29.36],[31.744,56.624],[58.624,66.992],[69.632,91.184],
    [ ... and many more ...]
  ]
}
```

Write a small component to consume the API and output a waveform (you can use svg or fixed sprites) to show a visualization for both channels, stacked on top of each other.


