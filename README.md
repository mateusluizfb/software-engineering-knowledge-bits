# Software Engineering Knowledge-bits
Just a repo with some texts that I think are important to remember from time to time

## Shape up - page 33:

Watch out for grab-bags:

When it comes to unclear ideas, the worst offenders are “redesigns” or “refactorings” that aren’t driven by a single problem or
use case. When someone proposes something like “redesign the
Files section,” that’s a grab-bag, not a project. It’s going to be very
hard to figure out what it means, where it starts, and where it ends.
Here’s a more productive starting point: “We need to rethink the
Files section because sharing multiple files takes too many steps.” 

Now we can start asking: What’s not working? In what context are
there too many steps? What parts of the existing design can stay the
same and what parts need to change?
A tell-tale sign of a grab-bag is the “2.0” label. We made the mistake
in the past of kicking off a “Files 2.0” project without really considering what that meant. Our excitement about improving a huge part
of our app got the better of us. We know there were a lot of problems with our Files feature, but we didn’t ask ourselves what specifically we were going to do. The project turned out to be a mess
because we didn’t know what “done” looked like. We recovered by
splitting the project into smaller projects, like “Better file previews”
and “Custom folder colors.” We set appetites and clear expectations
on each project and shipped them successfully.

