**Heads-up**  
This post originally appeared in my [employer's official blog](https://medium.com/@vptech/my-first-9-months-as-lead-of-a-development-team-at-vente-privee-3442bb9946c2)

-----------------------

![_config.yml]({{ site.baseurl }}/images/steps.jpeg)

On January 2018 my current employer, Vente-Privée.com. granted me with the opportunity to lead and manage the development team I was already working in as an individual contributor.

This was a first time for me, and if I look back at these nine months that have passed so far, I can see that I already learnt a lot on the job: some lessons have been learnt the hard way, while others via precious feedback from my team-mates; I also reinforced my belief in some well known software engineering principles, this time from the point of view of the one accountable for the success of the project and the well-being of the team, which certainly spices things up.

I'd like to share with you some of the principles that have proven to be the most effective to me.

## Focus

In my opinion this is the most important one, which enables many of the following points.

It's easy to feel overwhelmed with responsibilities, tasks, projects, meetings etc, and the key to come out of this mess is focus.

For example, at the beginning we were trying to build several software projects in parallel, and given we are a small team, this meant that only 1 or 2 people were really working together over each project and the result was that the team didn't feel like we were really a team neither advancing at a satisfying pace.

What worked for us was to assess the breadth and depth of the perimeter we had to cover, define important matters from a business and technical value point of view, and choose to focus almost solely on them.

Doing this affected our product roadmap, team organisation and, more in general, our approach to questioning if something was really worth our immediate attention when evaluating tasks.

As a consequence we decided to concentrate all our collective efforts on the most critical project and we started working together really as a team. That is not to say everything went smooth or without issues, but at least it allowed us to release to production and start collecting real feedback we could immediately reuse on this and other projects.

In the end, starting and finishing something (might be a milestone, an MVP etc...) is far better than starting several endeavours and not even completing one.

## Know the scope and master the perimeter (how the system will be used)

Knowing the reason we do something is important, but it's not enough. When designing a system, I found out it is quite important to understand how the system will be used by your upstream clients and which workloads might prove difficult to support: an example might be concurrent updates of a single entity where the cost of a single update is high.

This might prove difficult to generalise, but for line of business applications, it should be feasible.

About this point, I like to quote the [Hyrum's Law](http://www.hyrumslaw.com/)

>With a sufficient number of users of an API, it does not matter what you promise in the contract: all observable behaviors of your system will be depended on by somebody.

Ignoring this point might have a huge negative impact on the success of the project.

## Quick iterations

{Understand the requirement, code, test, deploy, observe} loop.

Strong requirements are

- having a reliable CI/CD that everyone in the team knows how to operate

- a versioning system and a changelog that allow everyone in the team to easily communicate changes to the upstreams

- an observation system (i.e. Prometheus+Grafana and/or ElasticSearch+Kibana) that is capable of clearly reporting how well the product is behaving based on expectations, and alert if issues arise

## Do it, do it right, do it better

Also known as `make it work, make it right, make it better`, this approach really shines if coupled with quick iterations.

It encourages to tackle risks from step one, to prove things are feasible and while focusing on solving the problem at hand, also avoids over-engineering the code base by adding premature abstractions which would only slow-down the development cycle for no obvious value.

About the differences amongst the steps, the `do it` phase focuses solely on having something that works and solves the problem, the `do it right` might focus on adding all those features necessary to ship to production, such as having logs and metrics or a clean interface. The last phase, `do it better`, can leverage production feedback to optimise some parts of the code base which proved slow, adapt the interface etc...

## Establish rules early on

One thing I learnt the hard way (i.e. by hitting a wall) is that what might be obvious to you might not be so for someone else.

That's why I think establishing a set of rules early on can help clearly communicate which culture should be favoured.

A few examples of rules are I used (or really should have used):

- Communication

- Be kind (see http://boz.com/articles/be-kind.html)

- Do not interrupt

- Before changing subject, be sure that everyone has said all they wish to say: some people are more shy than others and won't raise their hand to speak

- Run periodic 1:1 with people in the team: I've been quite surprised by the power of this tool and if done well, it's possible to learn a lot about the people you work with. A lot depends on the people as well, and a lot has to do with trust.

- Quality of work

- Help establish what quality means for the team and for the stakeholders. If needed, help write a quality document so that the whole team knows what's the expected code quality and things such as code reviews can be factual with comments referring to the document.

- Favour code readability and maintainability when in doubt

- Holidays

- To facilitate holiday planning, state what's the minimum number of people that should be present at any time in case of overlapping days off

- Operational rules

- Less is more: avoid infrastructure or architecture complexity unless necessary, design to favour operational and troubleshooting simplicity

- Favour production stability above all else

- Logging, monitoring and alerting are pre-requirements to go to production

- Promote a knowledge sharing culture amongst the team. Allow free time to keep up to date with latest news in tech, to write down proof-of-concept sw and to create a feedback loop to share things learnt with the team.

## Conclusions

I can't thank enough my team and the people I worked with, for having thought me many of those principles and rules: we learn by failing and by understanding why we failed, and sometimes by adopting wise advises :)