# Django Google Calendar Integration

## Overview
This project is a Django application that integrates with Google Calendar using the Django Rest Framework and the OAuth2 mechanism. The aim of the project is to retrieve a list of events from a user's Google Calendar.

## API Endpoints

The following API endpoints have been implemented:

### `/rest/v1/calendar/init/` - `GoogleCalendarInitView`
This endpoint initiates step 1 of the OAuth process and prompts the user for their Google credentials.

### `/rest/v1/calendar/redirect/` - `GoogleCalendarRedirectView`
This endpoint performs the following tasks:
- Handles the redirect request sent by Google with a code for the token
- Implements the mechanism to get the `access_token` from the given code
- Once the `access_token` is obtained, it retrieves a list of events from the user's calendar

## Requirements
- Django
- No third-party libraries, except for Google's standard libraries

Run the Django development server using the following command:

```python
python manage.py runserver
```