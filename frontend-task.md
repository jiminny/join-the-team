# Waveform Visualizer (Frontend Take-home Task)

The task solves a real-life problem related to converting an audio file into a useful waveform. Waveforms are a key way for our customers to visualize speech data.

We recommend writing answers in whatever language you’re most comfortable in. Like our own code, we expect testing instructions: whether it’s an automated test framework, or simple manual steps.

---

## Brief

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
You'll end up with something looking like this:
![waveform](./assets/waveform.png?raw=true "Waveform")

## Requirements

1. Consume the API to read the waveform data.

2. For each channel, output a waveform visualization in different colours. Silent gaps should be transparent.

3. Stack the channels with `user` on top, and `customer` below.

4. Highlight the longest segment for each channel with a different colour.

## Coding Standards

* Use git to version control the application
* Install a code linter and ensure it's passing
* Scaffolding should not be used to generate any MVC code
* Unit test validation rules
* Include instructions in a README on how to run the application and how to run the test suite

## Submission

Please publish your submission to GitHub or [jsfiddle.net](https://jsfiddle.net/).
