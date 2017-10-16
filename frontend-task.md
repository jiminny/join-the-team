# Waveform Visualizer (Frontend Take-home Task)

The task solves a real-life problem related to converting an audio file into a useful waveform. Waveforms are a key way for our customers to visualize speech data.

We recommend writing answers in whatever language you’re most comfortable in, using a component based framework. Like our own code, we expect testing instructions: whether it’s an automated test framework, or simple manual steps.

---

## Brief

You'll start with a simple REST API that returns a [JSON payload](https://rawgit.com/jiminny/join-the-team/master/assets/wavedata.json) with data from a real conference call. The information is related to a conversation between two parties. 

The response payload contains a simple array structure, the `user` channel, and the `customer` channel. Each channel contains an array of points that indicate when the audio channel was active (speech started), and when speech stopped (the order is important).

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

## Requirements

1. Consume the API to read the waveform data.

2. For each channel, output a waveform visualization in different colours. Silent gaps should be transparent.

3. Stack the channels with `user` on top, and `customer` below.

4. Hovering over waveform displays current time indicator (vertical line with time at the bottom).

5. Clicking on waveform shows add comment popover.

6. Enter key saves the comment to `localstorage`.

7. Comments have a `lightgreen` circle representation between the channels on the waveform.

8. Comments are rendered below waveform.

9. Comments can be deleted.

10. Implementation should be responsive.

11. At least one e2e test and one unit test should be provided.


You'll end up with something looking like this:
![waveform](./assets/waveform.png?raw=true "Waveform")

## Coding Standards

* Use git to version control the application
* Install a code linter and ensure it's passing
* Scaffolding should not be used to generate any MVC code
* Unit test validation rules
* Include instructions in a README on how to run the application and how to run the test suite

## Submission

Please publish your submission to GitHub or [jsfiddle.net](https://jsfiddle.net/).
