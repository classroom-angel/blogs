# Friday, April 5, 2019 - End of Week 3

## Individual Accomplishments this Sprint

This week, I worked on three main parts of the back end and front end. On Monday, I added more robust error messages to the POST to “create” endpoints on the back end, to make it a little more obvious when all the required fields weren’t included in the request. On Tuesday, I worked on a fetch endpoint for our image uploader package, Cloudinary. It helps pull images off their servers to send back to our front end app. On Wednesday and Thursday, I worked on our Stripe Connect integration. More details about that are in the next section.

## Detailed Analysis

For the Stripe integration, I had to do quite a bit of toying around to get Connect to work. Connect enables us to have a payments platform that contractors who work for our schools can get paid for the work they do. Rachel already implemented the subscription to our app on the front end using react-stripe-checkout and John had implemented an endpoint on the back end to create the actual charge to be sent to Stripe. I followed Stripe’s documentation on OAuth to get our Connect working. There was a 4-step process: 1) Create the OAuth link (this was easy), 2) User (in our case, contractor) creates or connects their account (also easy), 3) User is redirected back to your site (a little tougher, but I used a regex example to parse the URL parameters), and 4) Fetch the user’s credentials from Stripe (not easy at all, I was stuck on this for a long time). I was trying to do a POST request to their server and I kept getting different errors with different status codes. John helped me on Thursday and we tried a cURL request instead of the post, and it worked! I could send myself fake money. So he decided to make an endpoint on the back end to process requests using a cURL package and I would send the required information from the front end. This worked, too! So now we can add a connection for contractors, revoke access if needed, and send money while they’re connected to our platform.

## Weekly Reflection

Working with this team has been a dream come true. Everyone works hard and is accountable for their own actions and mistakes. Even so, there are times when we help each other fix issues, and they’re common. We have a great team dynamic. For example, I created some merge conflicts one day, and Jordan helped me clear them up in VS Code. That was awesome of her. She and Alec and Rachel have spent more time on the front end, so Jordan was in a better place of knowing what needed to be there and what was erroneous or duplicated. Merge conflicts are one of the bigger problems we have, as opposed to say, fighting. We haven’t had a single fight, and I’m sure it happens in some groups. I really appreciate my team!

## Pull requests/Trello Cards

- [More robust error messages Trello](https://trello.com/c/FJvW8kkN)
- [More robust error messages PR](https://github.com/classroom-angel/labs11_prop_mngmt-BE/pull/59)

- [Cloudinary back end fetch endpoint Trello](https://trello.com/c/Kg4sqQfO)
- [Cloudinary back end fetch endpoint PR](https://github.com/classroom-angel/labs11_prop_mngmt-BE/pull/62)

- [Stripe Connect Trello](https://trello.com/c/DVZFdakl)
- [Stripe Connect PR #1](https://github.com/classroom-angel/labs11_prop_mngmt-FE/pull/68)
- [Stripe Connect PR #2](https://github.com/classroom-angel/labs11_prop_mngmt-FE/pull/73)
