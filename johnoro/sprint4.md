# My favorite 4 P.R. links

- [Prettier](https://github.com/classroom-angel/labs11_prop_mngmt-FE/pull/105)
- [GET related org data](https://github.com/classroom-angel/labs11_prop_mngmt-BE/pull/76)
- [Breaking down long files](https://github.com/classroom-angel/labs11_prop_mngmt-FE/pull/144)
- [HTML docs](https://github.com/classroom-angel/labs11_prop_mngmt-BE/tree/html-docs)

## Individual Accomplishments this Sprint

I added prettier to the front end for uniform code formatting, touched little things up here and there, did an overhaul of the code itself for a few of our React components/pages, and turned our markdown documentation into HTML documentation that is much easier to navigate! I also attempted adding node mailer for sending links to contractors for hooking up to our stripe account, but I couldn't quite get the needed permissions and information from our domain to get it all set up correctly.

## Detailed Analysis

[Breaking down long files](https://github.com/classroom-angel/labs11_prop_mngmt-FE/pull/144) was probably the most tedious thing I worked on this week besides attempting to get node mailer set up (which involved trying and constantly failing at jumping through loops and supposed loopholes). This involved going through and finding similarities, bits of logic that didn't utilize state, and just pieces that could be moved out easily in the issues directory. Originally, there were only two files there (both being very long); now there are many more, with both of those files being shortened substantially; both still need work, though). To put this into perspective, the IssueLog component was originally 512 lines. I shortened it to 283 lines when all was said and done. For a more visual representation, the reader could go and look at the IssueLog code before on the linked PR and after on [this PR](https://github.com/classroom-angel/labs11_prop_mngmt-FE/pull/145). It really is night and day how much you _can_ break up, and how much easier it makes it for new eyes to sift through (especially when a lot of the scrolling becomes clicking a new, logical file instead).

## Milestone Reflections

I didn't focus on UX as much as I did cleaning other parts of the application up-- code, documentation, et cetera. We had some trouble with getting styling organized (we had some odd conflicting colors here and there), but we have it pretty sorted out now. Next week, I'm going to try to really iron out any and all bugs that I can.
