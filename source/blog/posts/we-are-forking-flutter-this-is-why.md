---
title: We're forking Flutter. This is why.
description: The Flutter team has a labor shortage. We're forking Flutter so that the community can accelerate Flutter's development.
publishDate: 2024-10-27
author: 
  name: Matt Carroll
  avatarUrl: https://secure.gravatar.com/avatar/2b519036dc508c11b0db3463fffbd8ff
---
Over the years, Flutter has attracted millions of developers who built user interfaces across
every platform. Flutter began as a UI toolkit for mobile - iOS and Android, only. Then Flutter
added support for web. Finally, Flutter expanded to Mac, Windows, and Linux. Across this massive
expansion of scope and responsibility, the Flutter team has only marginally increased its size.
To help expand Flutter's available labor, and accelerate development, we're creating a fork
of Flutter, called Flock.

## Flutter's labor shortage
Let's do some back-of-the-napkin math to appreciate the Flutter team's labor shortage.

How many Flutter developers exist in the world, today? My guess is that it's on the order of
1,000,000 developers. The real number is probably higher, but one million should be reasonably
conservative.

How large is the Flutter team, today? Google doesn't publish this information, but my guess is
that the team is about 50 people strong.

That's 50 people serving the needs of 1,000,000. Doing a little bit of division, that means
that every single member of the Flutter team is responsible for the needs of 20,000 Flutter
developers! That ratio is clearly unworkable for any semblance of customer support.

A labor shortage can always be fixed through hiring. However, due to company-wide issues
at Google, the Flutter team's head count was frozen circa 2023, and then earlier in 2024
we learned of a small number of layoffs. It seems that the team may now be expanding again,
through outsourcing, but we're not likely to see the Flutter team double or quadruple its
size any time soon.

To make matters worse, Google's corporate re-focus on AI caused the Flutter team to
de-prioritize all desktop platforms. As we speak, the Flutter team is in maintenance mode
for 3 of its 6 supported platforms. Desktop is quite possibly the greatest untapped value
for Flutter, but it's now mostly stagnant.

## The cost of limited labor
Limited labor comes at a great cost for a toolkit that has rapidly expanded its user base, along
with its overall scope.

With so few developers to work on tickets, many tickets linger in the backlog. They can easily linger
for years, if they're ever addressed at all.

By the time a member of the Flutter team begins to investigate a ticket, the ticket might be years
old. At that point, the Flutter team developer typically asks for further information from the person
who filed the ticket. In my experience, when this happens to me, I've long since stopped working with
the client who had the initial issue. I've written hundreds of thousands of lines of code since then.
I often don't even remember filing the issue, let alone the obscure details related to the original
issue. The team can't fix the bug without information from me, and it's been too long for me to provide
information to the team. So the bug gets buried for a future developer to rediscover.

Timing isn't just an issue for eventually root causing and fixing bugs. It's also a major product
problem. Imagine that you're the engineering director, or CTO of a company whose next release is
blocked by some Flutter bug. What do you do if the team won't work on that bug for 2 years? Well,
if it's a serious bug for your company, then you stop using Flutter. You don't have a choice. You
need to keep moving forward. Your team doesn't know how to work on the Flutter framework, and the
Flutter framework team is either unresponsive, or at least completely non-committal towards a
fix. Oh well - can't use Flutter any more. Flutter won't survive if these kinds of experiences become
common.

## The Flutter community can help with labor
Flutter has two very valuable qualities. First, it's open source, so any developer can see how
any part of Flutter is implemented, and can even change it. Second, the Flutter framework is
written in the same language as Flutter apps. Because of these two qualities, experienced Flutter 
app developers, and package developers can contribute to the Flutter framework.

How many Flutter developers exist in the world today who are capable of contributing at a 
productive level to the Flutter framework? Conservatively, I would guess there are about 1,000
of them. In other words, there are at least 1,000 Flutter developers in the world who could
conceivably be hired to the Flutter team, if the team wanted to hire that many developers.

Remember that ratio of 1 Flutter team member per 20,000 developers? If every capable Flutter
framework contributor in the world regularly contributed to Flutter, that ratio of 1:20,000
would drop to 1:1,000. That's still a big ratio, but it's **much** better than what it is
now.

Moreover, as more external contributors get comfortable submitting fixes and features to
Flutter, they'll tend to help train others to do the same. Thus, the support ratio would
continue to move in a better direction.

## Why not work directly with the Flutter team?
If increased external contributions is the path to a better Flutter world, then why fork
Flutter when everyone could just work directly with the Flutter team?

It's a tempting proposition to setup a concerted effort to contribute directly to Flutter.
After all, the Flutter team regularly touts the number of external contributions that it
rolls into each release. According to the Flutter public relations effort, they'd love all
those external contributions!

But, sadly, trying to work with the Flutter team delivers a different reality. While some
developers have had success working with the Flutter team, many other developers have found
it frustrating, if not unworkable. There are, no doubt, a number of factors that contribute
to this result. Different developers will experience different issues. But here are some of
them:

 * Limited review labor:
   * The developers who don't have enough time to write code are the same developers tapped
     to review contributions. Therefore, it can take a long time for review or updates.
   * The time crunch also seems to lend itself to contentious review conversations.
 * Everything takes forever, and it always seems to be about non-critical details.
 * Communication monoculture - most of the team seems to expect a certain way of communicating,
   which doesn't match the variety of personalities in the world. Thus, some people have an
   exceptionally difficult time navigating otherwise quick and simple conversations.

The result of the aforementioned issues, and probably others that aren't listed, is that the
total number of people who have ever contributed to the Flutter framework is currently less
than 1,500. That number includes people who dropped by, one time, to fix a typo in a Dart Doc
and then never contributed again. That's **not** the number of regular contributors who add 
significant value.

Whatever your experience with contributions to Flutter, one has to critically assess why a
team that loves external contributions has only managed to merge contributions from 1,500
developers over a span of nearly a decade. My humble suggestion is that it's because the
inviting message of the PR team doesn't match the experience of actually pushing a change
through the team's policies, developer availability, and technical culture.

The only people who can change this reality are the people within the Flutter organization.
However, most of those people don't actually think any of this is a problem. I know, because
a number of them have expressed this to me, directly. There are a number of significant blind
spots for the Flutter team, which largely revolve around the fact that members of the team
have never been responsible for routinely delivering app features and fixes that are built
upon Flutter. In other words, I believe there are blind spots because Flutter team members
don't actually use Flutter. Thus, the urgency around many issues isn't appreciated, nor is
the urgency and time cost associated with submitting fixes directly to Flutter as an
external contributor.

If the Flutter team doesn't recognize the contribution problem, and therefore won't take
steps to address it, then what else can be done? That's where we find ourselves in this
post, and in this effort. We've decided that the one thing we can do to help the labor
issue is to fork Flutter. 

## Introducing Flock
Our fork of Flutter is called Flock. We describe Flock as "Flutter+". In other words, we
**do not** want, or intend, to fork the Flutter community. Flock will remain constantly
up to date with Flutter. Flock will add important bug fixes, and popular community features,
which the Flutter team either can't, or won't implement.

By forking Flutter, we get to decide what gets merged. We won't lower the quality bar, but
by controlling merge decisions, we do gain the following opportunities:

 * Recruit a much larger PR review team than the Flutter team. This means faster review times.
 * Recruit PR reviewers who are ready to facilitate contributions, instead of merely tolerating them. 
   This means support for a wider contributor audience.
 * Optimize policies. E.g., don't blindly demand design docs and conference calls when they won't 
   substantially add to the effectiveness of the task at hand.
 * Use contribution successes to socially promote more contributions.
 * We're all Flutter users - leverage team and company relationships to identify market priority.

As Flock ships important bug fixes and features, the Flutter team can then choose to add those
to Flutter, on their schedule. The community will no longer be limited by the Flutter team's
availability, nor will the community need to beg the Flutter team to please accept a change. The
Flutter team can use Flock's solutions, or not, but all Flock users will have access to them,
eliminating your company and team's urgency and desperation.

## How you can get involved
Flock, as the name implies, will only go as far as the community that supports it. We would
love for you to get involved.

### Alpha test the fork
Flock's first step is to mirror Flutter. This means automatically mirroring the `master`, 
`beta`, and `stable` branches, along with replicating all release tags. Additionally,
once the framework is mirrored, Flock will need to automatically build and upload the
engine, and make those engine binaries available to Flock users.

As we work through the mirroring process, it would be a big help if you would try building
your apps with Flock. You shouldn't see any difference between Flock and Flutter, and you
can configure Flock with a tiny Flutter Version Manager (FVM) configuration.

Check our instructions to [get started](https://flutterfoundation.dev).

### Become a reviewer
Flock needs to recruit dozens of reviewers. Reviewers are responsible for enforcing a
quality bar that's similar to Flutter's. This includes requiring descriptive class, method,
and property names, effective Dart Docs, and appropriate tests. 

But we want reviewers to go even further than that. We don't just want to tolerate contributions -
we want to facilitate them. Many of us have had the experience of getting a PR 90% to the finish
line only to have a Flutter team reviewer declare that it can't merge until we do something that
we don't know how to do. It's an awful experience, and we aim to avoid it with Flock.

We want Flock reviewers who are willing to step in and help a contributor achieve the final 10% of
the PR. This doesn't mean contributors get to be lazy. But if a contributor has done everything
that they know how to do, and the PR is close to complete, then we want the reviewer to step in
and provide direction for the final 10%. This is how we educate contributors and ensure that the
next PR is 100% complete.

If you'd like to become a Flock reviewer, [please reach out to us](https://x.com/suprdeclarative).

### Become a Lead
Maintaining and extending a long-lived fork of Flutter requires some number of experts who
direct specific areas of the project. For example, I'm initially stepping up at the Director
of Flock, as well as the Framework Lead. Jesse Ezell has stepped up as the Engine Lead.

We'd like to bring in a Flutter Tool lead, who directs extensions to the `flutter` CLI tool.

We'd also like to break up the engine responsibilities with a Lead per platform: Android, iOS,
Mac, Windows, Linux.

If you'd like to direct efforts for an area of Flock, [please reach out to us](https://x.com/suprdeclarative).

## Let's Flock together
Let's shift Flutter into overdrive and help make it the universal UI toolkit it should
have been. Flutter has the potential to outshine every alternative in the market. But
it needs the community to Flock together to help get it there. Let's do this!
