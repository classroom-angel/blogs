# My favorite 4 P.R. links

- [Database seeding](https://github.com/classroom-angel/labs11_prop_mngmt-BE/pull/20)
- [Nice responses, plus a bugfix](https://github.com/classroom-angel/labs11_prop_mngmt-BE/pull/35)
- [Organization FE route outlines](https://github.com/classroom-angel/labs11_prop_mngmt-FE/pull/29)
- [Some stripe](https://github.com/classroom-angel/labs11_prop_mngmt-BE/pull/55)

## Individual Accomplishments this Sprint

A lot of my time was spent just building out the rest of the C.R.U.D. routes for everything left. After that was done, I also spent a good amount of time linking the many to many relationships in an at least semi-logical way. After that, I spent the rest of my time helping out with some other implementation details (like with stripe) and with cleaning up our code (making sure that certain files aren't twice as long as they need to be for no reason).

## Detailed Analysis

Let's take [this P.R.](https://github.com/classroom-angel/labs11_prop_mngmt-BE/pull/46) as it'll show off a bit of the mundane, which seems to be a good summary for the majority of my work this week. The following code is the highlight:
```javascript
const camelToSnakeCase = str =>
  str.replace(/[A-Z]/g, letter => '_' + letter.toLowerCase());

const snakeToCamelCase = str =>
  str
    .split('_')
    .map((word, ind) => {
      if (ind) {
        return word[0].toUpperCase() + word.slice(1);
      } else return word;
    })
    .join('');

const keysToCamelCase = obj => {
  const keys = Object.keys(obj);
  const newObj = {};

  for (let key of keys) {
    newObj[snakeToCamelCase(key)] = obj[key];
  }

  return newObj;
};

const db = require('../dbConfig');
const joinIssue = async (obj, table, single) => {
  const [joinIssue] = await db(`issues_join_${table}`)
    .where({ [`${single}_id`]: obj.id })
    .returning('*');

  if (joinIssue) {
    return { ...obj, issueId: joinIssue.issue_id };
  }

  return obj;
};
```
which is just used for some of the file stuff (so as to get rid of the need for managing imports and exports in an index file or two), and then for transforming some of the data being sent back. The rest of the code is repetitive, making adjustments for these helpers where applicable.

## Milestone Reflections

I feel like with how we got set up week one (with a nice, efficient git flow and with everyone having a bit of familiarity with each other) set us up for success. 
I've worked outside of hours a couple of days now, but that hasn't been due to anything other than my desire to learn new stuff (or, more specifically, my desire to figure out problems that seem difficult). I'm not so sure that that causes friction, but I'm at least aware that we, our labs team, do affect each other with how we work and when we work. If I were to be putting in extra hours every day, that might be a cause for friction, as others could feel like they _need_ to put in more as well. I just need to watch myself as it's often the working people themselves who the set tone!
I simply and honestly state my opinions on things. I try to encourage others to do so as well, but mainly by leading by example when I do have something substantive to say. I've been more vocal about certain things (like our git flow) due to my experience of seeing what works well and what doesn't work quite as well.
Here's a summary of my git flow (compared to the proposed git flow requiring a project manager who is typically managing more than just one project to merge into the working branch for the team):

In regards to the git flow presented, after being a project manager for and being involved in a bunch of build week groups along with two (now three I suppose) labs groups, having a flow that depends on the project manager is a bit backwards. It'd be different if every P.M. only had one group, but they don't. They really can't be involved enough to give thorough reviews that consider everything in the scope of the app, and, even if they do, it'll dramatically slow down development. Here is an alternative that I've seen work very well:
- No forking!
- Create a feature branch named appropriately (i.e. `register-user-api`).
- Do all of your work for that feature off of that feature branch.
- When work on a feature is complete, create a P.R. with the base branch being `development`.
- Add a team member as a reviewer of the pull request. It will be mergeable after it has been reviewed and approved (we'll use a special merge rule for this).
- Each day roughly, we'll make one big final P.R. from `development` to `master`. This is when the code will get deployed to production (both branches will be deployed identically; `development` is what'll be used for testing, and `master` solely for the production app).

Our team has ended up with only a single deployment (of the `development` branch) and we don't always enforce the review rule, but it's worked out extremely well for us. Any merge conflicts (the ones I've encountered can be counted on one hand, maybe two hands if you count the ones that I've caused and fixed myself) have been solved within a minute or two, and development has went a lot faster than it would have otherwise. Having a feature branch to make a P.R. with and then being able to hop on to the next feature on a new branch is great for the review flow as well.
