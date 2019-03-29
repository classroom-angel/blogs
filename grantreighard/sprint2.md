# Friday March 29, 2019 - End of Week 2

## Individual Accomplishments this Sprint

This Sprint, I was very productive. I finished full CRUD for users, organizations, solutions, and teacher attendance. I added API documentation, after we tried to use an NPM package called Swagger to make it for us automatically and it didn’t work. I added “get by ID” routes for all of the categories of our data to get single objects back. I also added a bunch of unit tests so we can test what keys the objects we get back from the server have.

## Detailed Analysis

For the unit tests, I installed Mocha and Chai, some testing packages. I wanted to model the tests off of some old ones we did during testing week, so I tried Jest, too, another testing package. I also installed Supertest to be able to make requests to the server. Jest didn’t work for me, it gave me an error of some type. So I went back to Mocha and Chai, using Chai expect statements. The syntax is only slightly different from Jest. I made some basic tests to make sure the server works and returns a response at the root and a status code of 200. Then I made tests for every endpoint we have, expecting keys on the return objects.

## Weekly Reflection

We picked our team while we were still PMing. We were all in the same original cohort together, except for Alec, so we were pretty close as it was. I don’t think we really needed to do anything to solidify us as a team. Our constant communication has been a blessing, and we’re mostly avoiding merge conflicts. There really hasn’t been much friction in the whole process. What I’m doing to make sure everyone has a voice in the decision process is to ask everyone for input when we do make decisions, and we go by majority.

## Pull requests/Trello cards

- [Write some unit tests Trello](https://trello.com/c/tMxsk36P)
- [Write some unit tests PR](https://github.com/classroom-angel/labs11_prop_mngmt-BE/pull/45)

- [Add get by ID routes Trello](https://trello.com/c/osHs1mIP)
- [Add get by ID routes PR](https://github.com/classroom-angel/labs11_prop_mngmt-BE/pull/39)

- [Add API docs Trello](https://trello.com/c/gwOjvOIs)
- [Add API docs PR](https://github.com/classroom-angel/labs11_prop_mngmt-BE/pull/36)

- [CRUD for teacher attendance Trello](https://trello.com/c/OFocEpj5)
- [CRUD for teacher attendance PR](https://github.com/classroom-angel/labs11_prop_mngmt-BE/pull/33)
