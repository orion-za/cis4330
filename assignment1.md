The main benefit of switching to microservices is that they make continuous deployment easier. For this reason microservices are used by large and successful companies
such as Amazon and Netflix, but this doesn't mean they are appropriate for all companies. After all, most companies aren't nearly as demanding as Amazon.

Where microservices *are* appropriate, their advantage over a monolithic code base is that they allow new features to be rolled out without
breaking the entire system. When you are rolling up multiple updates every day through CD, this is obviously crucial. The key to effectively implementing
microservice architecture is balancing granularity with complexity. Microservices replresent te most "fine-grained" end of the granularity spectrum and are appopriate
for programs with extreme agility requirements. "Miniservices" are the middle of the spectrum, and they provide some of the agility of microservices without the disrpuptiveness.
Unlike microservices, they may implement more than one feature in a single service. Many companies think they need microservices when miniservices would be more appropriate.
On the "coarse-grained" end of the spectrum are "macroservices", or traditional APIs within a monolithic system. A single application may use multiple levels
of granularity.

I think that the rise of microservices represents a new challenge for software architects. Because they are trendy, many will attempt to switch to a microservice architecture
when it is really not appropriate. On the other hand, vendors may claim to offer microservices when they are really offering something else, for example REST APIs or
containers. I think that as time passes and "new toy syndrome" fades, more people will understand what a microservice really is and when they should be used.

