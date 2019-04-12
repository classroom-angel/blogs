# My favorite 4 P.R. links

- [Image uploading with Cloudinary](https://github.com/classroom-angel/labs11_prop_mngmt-BE/pull/60)
- [Stripe Connect BE](https://github.com/classroom-angel/labs11_prop_mngmt-BE/pull/69)
- [How does one send data?](https://github.com/classroom-angel/labs11_prop_mngmt-BE/pull/70)
- [Stripe subscription](https://github.com/classroom-angel/labs11_prop_mngmt-BE/pull/74)

## Individual Accomplishments this Sprint

A lot of my work was research for how to use a certain API or to help out others with their specific problems. I got to use a couple flavors of Stripe (connect for user-to-user payments and subscription stuff for recurring payments). I got back end C.I. working with travisCI. I updated the models a little bit to fit with our requirements. I also got to help others here and there for the sake of getting everything tied together (and, feature-wise, the app is really coming along now; we're just about done with everything). I also think [this commit](https://github.com/classroom-angel/labs11_prop_mngmt-FE/pull/56/commits/cf6be8a165bd89fbab0ffc3046a78ddad34163ce) is worthy mentioning just because of the tiny but significant difference it makes in terms of readability and reusability. As for the readability bit, I think the F.E. definitely needs to integrate a code formatter like prettier (with forced settings like on the B.E.). I'll probably push for that sometime today or Monday.

## Detailed Analysis

Let's choose the [stripe subscription](https://trello.com/c/WxiqWhwl/71-add-subscription-to-stripe) stuff. This one wasn't anything too fancy, but it involved(/involves) a few things:
- initially, getting everything connected and working with stripe (specifically with single payments)
- obscuring away secret keys (via dotenv)
- cleaning up the organization of the files
- accidentally using an unresolved promise as if it was resolved
- fixing that 
- adding an extra optional field (the email is optional as well)
- sticking it in a try with a catch to boot
- cleaning up the front end
- adding a token helper for subscriptions
- profit (once we stop using our test key)

## Milestone Reflections

I spent a lot more time this week just working with team members on what they were working on or with things we both were trying to implement [parts of]. We're getting pretty close to having everything complete, but we still have a good bit of work to do on styling. We'll be hitting that hard next week. On a few days, my brain got to a mushy-feeling point earlier than the time that we were done. That always slows things down a bit. The FE part of the project also seemed to have more merge conflicts this week than usual, but I think that's because some people were getting a little too gungho about what all they were editing without letting others know (I think one pretty bad merge conflict that Grant had was caused by me, but I did ping about it at least). I tried helping out with that since I use git a lot, but I think we ended up going with a moving files around type of solution.
