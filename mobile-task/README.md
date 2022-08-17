# Jiminny Filter Form
![This is a alt text.](/mobile-task/form_screen.png "Form screen")
![This is a alt text.](/mobile-task/resuluts_screen.png "This is a sample image.")

## Brief
This task is about creating a form which you can use to filter through an array of recorded meetings.

The first screenshot shows how the form should look like and the second screenshot shows the results when the "Show Results" button was pressed.

Inside <b>assets/meetings.json</b> file you'll find an array of sample data.
Each object has the same number of properties, all required and represents a meeting(or at least tiny fraction of a real one).
> {
"title" : "Title of the meeting",
"userPhoto": "Image of the organizer",
"notetakerAddedOn" : "Datetime | When the notetaker was added on",
"createdAt" : "Datetime | When the record was created",
"timeAgo" : "human readable time format",
"platform" : "The crm platform which the customer is currently using",
"teamMember" : "A member of the organization",
"customer" : "The name of the customer"
}

Inside <b>assets/saved_search.json</b> file you'll find an array with pre-defined search criteria.
Our reps use this to reduce the time spent on common searches.
All properties except <b>title</b> can be null.
> {
"title" : "Lauren Sessions",
"teamMember": "Lauren"|null,
"platform": "Salesforce"|null,
"customer": "BMW"|null
}

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
3. In order to submit the form <b>at least one</b> filter input** must have a value.
4. When the form is submitted, all the meetings should be filtered using the data from the form. The criteria for input value to meeting property goes as it follows: Platform => platform, Team Member => teamMember, Customer => customer.

5.Redirect the user to the second screen and list all the filtered meetings.

** Filter inputs are inputs located below the <b>Filter</b> section.

## Coding Standards
* Ideally use git to version control the application
* Include instructions in a README on how to run the application, if needed.

## Bonus points
You'll get extra points if:
- State Management Solution is included
- Your code is covered by tests.

## Submission
Please publish your submission to GitHub.