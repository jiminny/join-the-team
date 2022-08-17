# Jiminny Filter Form
![This is a alt text.](/mobile-task/form_screen.png "Form screen")
![This is a alt text.](/mobile-task/resuluts_screen.png "This is a sample image.")

## Brief
This task is about creating a form which you can use to filter our activity content.
The first screenshot shows how the form should look like and the second screenshot shows the results  when the "Show Results" button was pressed.

You are free to use any packages.
Please use the latest Flutter version, if possible.

## The form
Our form contains the following inputs**:

1. Saved Searches - Dropdown field with dynamic values located in <b>assets/saved_search.json</b>
2. Platform [Salesforce, HubSpot] - Dropdown field. Only one option can be selected.
3. Team Member [Alice, Tom, Lauren] - Dropdown field. Only one option can be selected.
4. Customer - Free text field.

** Values are listed in the square brackets when possible.

## Requirements
1. The design should be as close to the screenshots as possible.
2. Changing the value of <b>Saved Searches</b> should populate the values of the other inputs depending on what's selected.
3. In order to submit the form at <b>least one</b> filter input* must have a value.
4. When the form is submitted, all the activities located in <b>assets/activities.json</b> should be filtered using the data from the form. Redirect the user to the second screen afterwards and list all the filtered activities.

## Bonus points
You'll get extra points if:
- State Management Solution is included
- Your code is covered by tests.

## Submission

Please publish your submission to GitHub or email us a zip or tarball of your prototype.