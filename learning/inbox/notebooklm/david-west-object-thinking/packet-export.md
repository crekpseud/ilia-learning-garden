# Reflections on David West's Object Thinking

## Source List

*   Title: CodeQualityAndReadability/Articles/BookReviews/ObjectThinking.md
    *   Author: Kasper B. Graversen
    *   URL: https://github.com/kbilsted/CodeQualityAndReadability/blob/master/Articles/BookReviews/ObjectThinking.md
    *   Description: A critical review of the book that highlights its philosophical nature and lack of concrete code examples, framing it as a "strange creation" in computer literature.
*   Title: Object Thinking By David West
    *   Author: Ben Nadel
    *   URL: https://bennadel.com/2483
    *   Description: A personal reflection on the book's impact, focusing on the difficulty of transitioning from procedural to object-oriented mindsets and the placement of business constraints.
*   Title: Object Thinking – David West, Ph.D.
    *   Author: David West
    *   URL: http://davewest.us/product/object-thinking/
    *   Description: The author's own landing page for the book, providing chapter summaries and the core contention that mindset, not tools, makes the programmer.
*   Title: Review of 'Object Thinking' - Linux.com
    *   Author: TechBookReport
    *   URL: https://www.linux.com/news/review-object-thinking/
    *   Description: An analytical review focusing on the clash between formalist (tools-led) and hermeneutic (people-led) approaches to software development.
*   Title: What It Means to Domain-Drive Your Design
    *   Author: Christian Tietze
    *   URL: https://christiantietze.de/posts/2015/10/domain-drive-design-david-west/
    *   Description: A blog post connecting West's concepts of object thinking to Domain-Driven Design (DDD), specifically regarding the modeling of problem domains versus solution spaces.
*   Title: Why NULL is Bad?
    *   Author: Yegor Bugayenko
    *   URL: https://www.yegor256.com/2014/05/13/why-null-is-bad.html
    *   Description: A provocative technical article and comments section arguing against the use of NULL in OOP, heavily citing David West as a primary influence.
*   Title: Object Thinking, David West Chapter 9 (All the World’s a Stage)
    *   Author: David West
    *   URL: http://davewest.us/wp-content/uploads/2016/10/otChap9.pdf
    *   Description: A deep dive into application architecture, the Model-View-Coordinator pattern, and the implementation of self-evaluating rules as first-class objects.
*   Title: Object Thinking, David West Preface
    *   Author: David West
    *   URL: http://davewest.us/wp-content/uploads/2016/10/otPreface.pdf
    *   Description: The book's introduction, contrasting "scientific management" (Taylorism) with the need for better developers through improved thinking and attitude.
*   Title: object thinking | malvasia bianca
    *   Author: David Carlton
    *   URL: https://malvasiabianca.org/2013/06/object-thinking/
    *   Description: A reflective post considering the applicability of object thinking to different software quadrants, such as "natural-sociocultural" vs. "deterministic" worlds.

## Learning Summary

This notebook explores the philosophical and behavioral foundation of software development as proposed by David West in *Object Thinking*. It challenges the prevailing "formalist" paradigm—which views software as a machine built of data structures and algorithms—and proposes a "hermeneutic" or behavioral view where software is a community of autonomous, collaborating objects. This relates to [[wiki/synthesis/digital-garden-ethos]] by treating software not as a static artifact to be "engineered," but as a living system that is grown and evolved. The sources highlight a significant tension: while West’s "object-as-person" metaphor provides deep conceptual clarity for domain modeling, it often leaves pragmatic developers frustrated by a lack of concrete implementation guidance. In the context of AI-assisted knowledge work, these concepts suggest that we should aim to model the "intrinsic talent" of objects (or agents) rather than hard-coding situational constraints, allowing for more composable and adaptable systems.

## Key Ideas

*   **Mindset over Tools**: The essence of OOP is a specific mindset ("object thinking") rather than the use of specific languages or techniques.
*   **The Object-as-Person Metaphor**: Objects should be conceptualized as autonomous individuals with responsibilities and "talents" rather than passive data entities to be manipulated.
*   **Hermeneutics vs. Formalism**: Software development is a clash between a rigid, tools-led "scientific management" approach and a people-led, interpretive, and agile approach.
*   **Behavior-Driven Discovery**: Objects should be identified and defined by their behaviors and responsibilities within a domain, not by their internal data structures.
*   **Rejection of NULL**: NULL is viewed as a procedural habit that breaks the object paradigm; it should be replaced by "Null Objects" that provide default behavior or by throwing exceptions.
*   **Situational vs. Intrinsic Rules**: Most business rules are situational (application-specific) and should not be baked into the intrinsic definition of domain objects.
*   **Self-Evaluating Rules**: Rules themselves should be first-class objects capable of modifying and evaluating themselves, reducing the need for centralized "manager" objects.
*   **Software as a Living System**: Large systems are viewed as "The System"—the complex whole of the domain, including human participants and patterned interactions.

## Candidate Concept Notes

### Object Thinking
*   Status: new candidate
*   Definition: A philosophical and behavioral approach to software development that prioritizes the conceptualization of software as a community of autonomous, collaborating objects over formal methods and data-centric modeling.
*   Why it matters: It shifts the focus from technical implementation to domain understanding and behavioral decomposition, aiming for order-of-magnitude improvements in adaptability.
*   Possible aliases: Behavioral OOP, Hermeneutic Software Design.
*   Related existing notes: [[wiki/synthesis/digital-garden-ethos]], [[wiki/synthesis/technopastoral-synthesis]].
*   Promotion recommendation: yes

### Null Object Pattern
*   Status: new candidate
*   Definition: A design pattern where a "nothing" or "empty" state is represented by a real object that implements a common interface but provides neutral or default behavior, rather than using a NULL reference.
*   Why it matters: It maintains the object-oriented paradigm of "sending messages to objects" without needing constant ad-hoc NULL checks that pollute code and cause runtime failures.
*   Possible aliases: Stub Object, Active Nothing.
*   Related existing notes: none.
*   Promotion recommendation: maybe

### Software-as-Theater Metaphor
*   Status: new candidate
*   Definition: A conceptual framework where software development is seen as casting actors (objects) with intrinsic talents into roles directed by scripts (application logic) on a stage (operating environment).
*   Why it matters: It emphasizes the separation between the intrinsic nature of an object and the situational roles it plays, preventing objects from being "typecast" into narrow, brittle application-specific definitions.
*   Possible aliases: Dramaturgical Software Design, Actor Metaphor.
*   Related existing notes: [[wiki/synthesis/digital-garden-ethos]].
*   Promotion recommendation: yes

### Self-Evaluating Rule
*   Status: new candidate
*   Definition: An architectural pattern where business rules are implemented as first-class objects capable of self-modification and evaluation, rather than being hard-coded into object methods or managed by external controllers.
*   Why it matters: It decentralizes control and makes business logic highly flexible and modifiable at runtime without recompilation, aligning with the "everything is an object" principle.
*   Possible aliases: Executable Rules, First-Class Constraints.
*   Related existing notes: none.
*   Promotion recommendation: maybe

## Important Claims

*   **Mindset is the primary bottleneck**: "the mindset makes the programmer—not the tools and techniques".
*   **The "Software Crisis" is a human problem**: Increasing the supply of highly skilled people is the only way to resolve the crisis, as Taylorist management methods have failed for forty years.
*   **"Everything is an Object"**: This dictum provides a single metaphor to partition even the most complex domains into manageable parts.
*   **NULL is a "Billion Dollar Mistake"**: The use of NULL references is a procedural inheritance that causes ambiguous semantics and "slow failing" code.
*   **Object creation should be encapsulated**: Naked constructors are viewed as a "code smell"; objects should be created through factory-like methods in collections or contexts.
*   **Most objects have very little interesting state**: A properly designed object hides its state behind an encapsulation barrier and focuses on behavior.

## Questions And Uncertainties

*   **Translation to Code**: How can the high-level philosophical metaphors of West be translated into concrete, performant code without becoming "psycho-babble" or "snake oil"?.
*   **The Role of Static Typing**: Do modern type systems (like those in Kotlin or Haskell) solve the problems West attributes to NULL better than the behavioral "Null Object" pattern?.
*   **Pragmatism vs. Purity**: When does the pursuit of "pure" object thinking become an obstacle to shipping software in a "ruthlessly pragmatic" environment?.
*   **Applicability Boundaries**: Is object thinking truly inappropriate for "close to the machine" or purely "deterministic" work, and where is the line between those and "natural-sociocultural" systems?.
*   **Human Factor in Delegation**: If logic is distributed and objects must collaborate, how do we prevent the "mental block" of wondering if the human developer forgot to write the collaboration correctly?.

## Suggested Trusted Wiki Output

*   NEW CANDIDATE: Object Thinking and the Digital Garden (Synthesis Note)
*   NEW CANDIDATE: Object Thinking
*   NEW CANDIDATE: Software-as-Theater Metaphor
*   NEW CANDIDATE: Self-Evaluating Rule
*   NEW CANDIDATE: Null Object Pattern
*   Suggested Patch to [[wiki/synthesis/digital-garden-ethos]]: Add a section on "Software as Community" drawing from David West's critique of scientific management and the "object-as-person" metaphor to strengthen the living-system framing.
*   Suggested Patch to [[wiki/concepts/digital-garden]]: Explicitly link the concept of "linked, evolving, contextual" notes to West's view of "The System" as a complex whole of patterned interactions between objects.

## Human-Contact Artifact

Include the supplied human-contact artifact:
**Software as a Community Not a Machine** [Audio Overview] - Ready (Customization: "Generate a deep-dive conversation between two technical analysts exploring David West's 'Object Thinking.' The discussion should contrast the 'Formalist' (structured, data-driven) approach with the 'Hermeneutic' (behavioral, agile) approach to software. Key points must include the 'object as a person' metaphor, why 'everything is an object' (including rules), and the book's controversial stance on common practices like getters/setters and the use of NULL. The tone should be analytical yet accessible, reflecting on why the book has a 'love it or hate it' reputation among pragmatic developers while offering high-level architectural insights like the Model-View-Coordinator pattern and self-evaluating rules.")
