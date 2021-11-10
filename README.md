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

# Domain Drive Design - page 103

Services:

Sometimes, it just isn't a thing.

In some cases, the clearest and most pragmatic design includes operations that do not
conceptually belong to any object. Rather than force the issue, we can follow the natural contours
of the problem space and include SERVICES explicitly in the model.
There are important domain operations that can't find a natural home in an ENTITY or VALUE
OBJECT. Some of these are intrinsically activities or actions, not things, but since our modeling
paradigm is objects, we try to fit them into objects anyway.

Now, the more common mistake is to give up too easily on fitting the behavior into an appropriate
object, gradually slipping toward procedural programming. But when we force an operation into an
object that doesn't fit the object's definition, the object loses its conceptual clarity and becomes
hard to understand or refactor. Complex operations can easily swamp a simple object, obscuring
its role. And because these operations often draw together many domain objects, coordinating
them and putting them into action, the added responsibility will create dependencies on all those
objects, tangling concepts that could be understood independently.

Sometimes services masquerade as model objects, appearing as objects with no meaning beyond
doing some operation. These "doers" end up with names ending in "Manager" and the like. They
have no state of their own nor any meaning in the domain beyond the operation they host. Still, at
least this solution gives these distinct behaviors a home without messing up a real model object.

Some concepts from the domain aren't natural to model as objects. Forcing the
required domain functionality to be the responsibility of an ENTITY or VALUE either
distorts the definition of a model-based object or adds meaningless artificial objects.
