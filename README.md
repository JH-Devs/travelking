Coding challenge for Front-end Developer - Travelking 2024
As you may have already found out / heard, Travelking is a travel agency that offers stays,
so in our business it is crucial to show potential customer stay options, mainly prices and
availability.
Your challenge from us will be to display such data, provided by API endpoint from our
parent company, Travelcircus.
We ask you to develop a simple site containing just a button, that upon clicking this button
will check availabilities and prices for 6 months in advance for 2 adults (already in endpoint
URL) beginning from current month and displays relevant info from endpoint to customer in a
calendar format. Calendar should be in an overlay format (popup). User should be able to
have a feeling which dates are available and how much it costs.
When customer selects his desired stay (variable number of days), and clicks on a button in
this popup, your site will then call another API endpoint and show him available rooms for
this date. That’s all, you don’t have to continue further.
API endpoints:
https://api.travelcircus.net/hotels/17080/checkins?E&party=%7B%22adults%22:2,%22childre
n%22:%5B%5D%7D&domain=de&date_start=2025-01-01&date_end=2025-06-31
this is the main availability endpoint that returns JSON of dates, each containing some useful
info that you should incorporate:
{
"date": "2025-01-05", // day
"price": 198,
"min_nights": 2, // minimum nights bookable from this date
"cheapest": true,
"price_position": "low" // used to determine color of price in calendar (price points)
},
After user chooses his/her preferred dates, you should call URL endpoint such as:
https://api.travelcircus.net/hotels/17080/quotes?locale=de_DE&checkin=2024-12-20&checko
ut=2024-12-23&party=%7B%22adults%22:2,%22children%22:[]%7D&domain=de
where you substitute the check in / out dates selected by customer. This endpoint returns
information about available rooms which you should then display for customer. This API
endpoint has a lot of information about rooms available so we leave it to you what you can
display.
You can see the challenge in action here: https://www.travelcircus.de/allegria-resort
This is by no means a test, we just want to get a general feeling of how you will handle more
complicated tasks, but you can google away or use any 3rd party library, we even
recommend using 3rd party library for the calendar itself (we for example use flatpickr, but
feel free to choose anything else). We want to know how you structure your code, how tidy
you are and how you approach problems.
Regarding the HTML/design part, we give you free hand to design the user interface in any
way you want, it should basically revolve around a button, popup, and displaying relevant
information to customer. This should tell us about your UX skills and feeling for basic graphic
design. You have various information for calendar and rooms available from APIs and it’s up
to you what you decide to use.
You don’t have to spend a lot of time with design itself, we are not here to judge that as you
will when you get the job, always be provided with graphic design in Figma from our graphic
designer.
We only ask you to not use any Javascript frameworks (Vue, React, etc.) and stick only to
vanilla Javascript. You can use any package manager, preprocessor, etc.
Your output should be:
- a single HTML file containing built source of the challenge
- a github repository (publicly accessible) with source code
