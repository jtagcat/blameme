# blameme
Blame me! — self-codeownering solution allowing you to subscribe to lines you've committed.

Yet an another idea repo, without any practical implementation.

Sometimes I _really_ want to know when a file or something in a directory has changed. I do this with RSS feeds, mostly [RSSHub](https://github.com/DIYgod/RSSHub).

If it was automatic, or one-click subscribe, I'd likely subscribe to many more directories / files / regex? (only certain files in directories).

What about automatically subscribing, and less noise (by filtering/scoping the subscription)?

***

There are a few components I'd see to this service:
 - Auth: private repos (and github enterprise) as well
 - Single-click subscribe
 - Dashboard: Userscript or extension (secuwurity?) (or website) to the gh notifications page:
   - because it's not natively implemented
   - also seperate it from the native notifications, since normal notifs (mention, comment to issue) is likely to be of more importance (or not?)
   - show that you have new stuff right there, the user shouldn't remember to check some page
 - Blame subscriptions (the ~~uhh main~~ flagship feature here):
   - track 'git' blame, stuff you've commited
   - allows scoped tracking within large files, where you have your section
     - (line-based tracking doesn't work since line numbers change)
   - not sure whether it's a good idea to only track changes made as you're the last to be blamed, or based on if you've ever been blamed (if the code is changed twice)
     - the whole section could get removed
     - also would likely mud up the quality
     - yeah, probably only track latest changes
     - though risk is, that you ignroe that one thing or forget to re-subscribe by other means, and poof
   - subscribing to other people's blames should be a thing as well
     - both in other's and self: scope a blame (even more quality, woot):
       - when you'd subscribe to all changes in the commit, instead select files or current line numbers to track
       - it's like instead of `goto line_number`, you use `goto label`; should be intuitive enough


A nice-to-have would to make it dumb easy to adopt: say, a project expecting, that you subscribe to a thing / area.
