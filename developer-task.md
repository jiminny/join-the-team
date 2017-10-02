# Jiminny Developer Take Home Project

There are specific tasks for both frontend and backend roles.

We recommend writing answers in whatever language you’re most comfortable in. Like our own code, we expect testing instructions: whether it’s an automated test framework, or simple manual steps.

You might find [gist.github.com](https://gist.github.com/) or [jsfiddle.net](https://jsfiddle.net/) a convenient way to send us your work.

---
## Waveform Visualizer

Waveforms are a key way for our customers to visualize speech data. You'll start with a real [JSON payload](https://rawgit.com/jiminny/join-the-team/master/assets/wavedata.json) from a conference call.

Here you’ll interact with a REST API that returns information about a conversation between two parties.
The payload contains a simple array structure, the `user` channel, and the `customer` channel.

Each channel contains an array of decimals that indicate when the audio channel was active (speech started), and when speech stopped (the order is important).
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


Write a small component to consume the API and output a waveform (you can use svg) to show a visualization for both channels, stacked on top of each another.
