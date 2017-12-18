# Conference Tests (QA Take-home Task)

The task attempts to mimic the real-world usage of the Web Conference product, trying to find problems before our customers do. Integration tests are a key way for us to cover a wide range of potential issues and ensure expected behaviour after each code commit.

We recommend writing the solution in whatever language you’re most comfortable in. The Selenium framework should be used alongside the necessary drivers.

---

## Brief

The Web Conference product is an online meeting room where an organizer (e.g. the person hosting the meeting) can speak in real-time with up to 50 guests. Web Audio is provided to allow the guests to speak through their browser using Web RTC technology. Similarly, screen sharing and webcam features are available once a meeting has started.

The organizer needs to be present for the meeting to start, but guests can join at any time in a "waiting room". This task will focus on the waiting room functionality.

A [test conference room](https://app.staging.jiminny.com/veselin) is available to use for the purpose of these tests. Feel free to use this room and get to know all of the available features. The task scope covers only the conference guests (e.g. non organizer).

Write a program to connect two different guests to the conference. Guests are idenfitied by their email address. Your tests will ensure certain features are available as expected, and organizer-only features are not available.

## Requirements

1. Create a test to ensure an invalid email address cannot be used to join a Firefox 56+ user to the conference.

2. Join two different Firefox 56+ users to the conference. They should be permitted to join the conference with valid credentials. 

3. Attempt to join another guest with Safari 10. They should not be permitted to join the conference, and instead the Conference App download instructions should appear.

4. Ensure that the "Mute All" button does not appear in the left menu for any guest.

5. Guest 1 should post a chat message "Ping". Guest 2 should see this message, and reply with "Pong".

6. Add Computer Audio for both guests, ensuring the timer does not start once both are connected.

7. After being on hold in the waiting room for 10 seconds, both guests should logout and the login page should be visible again.

8. For every failure, a screenshot should be taken of the page.

## Coding Standards

* Use git to version control the application
* Include instructions in a README on how to run the test suite

## Submission

Please publish your submission to GitHub or email us a zip or tarball of your solution.

