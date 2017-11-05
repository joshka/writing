---
title: Draft License Zero Reciprocal Public License, Annotated
description: a terse, hacker-style superstrong copyleft license
layout: post
tags:
- Open Source
- licenses
- License Zero
---

I've just sent a complete rewrite of the draft License Zero Reciprocal Public License to the Open Source Initiative for review and approval.

If you have feedback on drafting, Open Source Definition conformance, or Open Source Initiative approval, you can [chime in with comments on the mailing list here](https://lists.opensource.org/pipermail/license-review/2017-October/003247.html).  If you'd like to express more general support or condemnation, feel free to e-mail me directly.  I'd like to keep the list discussion as focused as possible, which hasn't always been the case to date.

I'm excited about this draft.  I originally wrote L0-R based on the venerable two-clause BSD license.  The idea was to focus discussion on the new parts, by minimizing the amount of new language for review.  But in the end, hacking L0-R's new ideas into BSD's old structure cost more in new confusion than familiarity with the old parts was worth.  A few reviewers encouraged me to take a free hand, rewriting and structuring L0-R as I thought best.  I hesitated, but came around.  I'm glad I did.

First the whole text of the draft, then the whole text again, with notes inline, from my drafting process.

# The Draft

    License Zero Reciprocal Public License <version>

    Copyright: <name>

    Source: <source>

    **This software comes as is, without any warranty at all.
    As far as the law allows, those giving this license will
    not be liable for any damages related to this software or
    this license, for any kind of legal claim.**

    You may do everything with this software that would
    otherwise infringe copyright in this software, or any patent
    anyone giving this license has or obtains that would have
    read on this software just after any of their contributions,
    on these conditions:

    1. You must ensure that everyone who gets a copy of this
       software from you, in source code or any other form, also
       gets the complete text of this license and the copyright
       and source notices above.

    2. You may not make any legal claim against anyone accusing
       this software, or any derivative work based on it, of
       infringing any patent that would read on this software
       alone, without modification or extension.

    3. If you modify or extend this software, you must release
       source code for your modification or extension.

    4. If you include this software in a larger piece of
       software, you must release any source code for that
       larger piece of software that has not yet been released.

    5. If you run this software to analyze, modify, or generate
       software, you must release source code for that software.

    To release source code, you must license it to the public
    under either these terms or terms approved by the Open
    Source Initiative, and promptly publish it, in the preferred
    form for making modifications, to a freely accessible
    distribution system widely used for similarly licensed
    source code.

    Any unknowing failure to meet condition 3, 4, or 5 is
    excused if you release source code as required within 30
    days of becoming aware of the failure.

# With Comments

    License Zero Reciprocal Public License <version>

Some open source licenses have titles, and L0-R does, too.

I'll fill in the version with "1.0.0" when it stabilizes.

## Notices

    Copyright: <name>

A standard copyright notice, as at the top of MIT or BSD terms.

I'd almost rather do a "Licensor" notice, like Fair Source, and then drop the copyright notice entirely, to avoid the "what's the difference between 'licensor' and 'copyright holder'?" question.  But I think that would seem too strange, and achieve no better results, in practice.  I think it would mostly confuse people.

    Source: <URL or instructions>

A notice of where to find source code.  This blends elements of the standard copyright notice and elements like Apache-2.0's `NOTICE` file, which Apache uses to point to a website, from which you can get source.  All to the greater thrust of L0-R, doing more to get the source code for software that matters to people in their hands.

Note that condition 1 (coming up) requires preserving this source notice in copies, just like the copyright notice.  That should give more end users the freedom to inspect and hack for themselves, as well as to alleviate cases where a distributor might have preserved the license and notices, but wasn't too careful to preserve data about what code falls under it, like file-level header comments.

There's another connection, to the scope of the patent permission later on.  In order to tell which patents fall under that permission, you need access to revision history, so you can see who contributed what, and when.

## Disclaimer

    **This software comes as is, without any warranty at all.
    As far as the law allows, those giving this license will
    not be liable for any damages related to this software or
    this license, for any kind of legal claim.**

The usual disclaimer of all warranties and liability, much condensed.

There is "gotcha" case law out there paring back disclaimers and limits on liability for failing to list exactly this kind of damages, exactly that kind of claim, that being "advised of the possibility of such damages" doesn't matter, and so on.  The usual lawyerly response to those kinds of opinions, whatever court issues them, is to tack on all the terms for kinds of warranties, damages, and claims we happen to know, and then some.  In L0-R, I've taken a different approach, saying no more than I think I need to get the no-liability point across.  The desired result is general.  Specificity is rowing in the wrong direction.

Addressing those issues the usual way, with a taller and taller stalagmite of legal terms, accreting over the ages, is ultimately self-defeating:

  1.  The more specific-sounding words you use, the more the language reads with intent to disclaim and limit specific legal risks.  When the intent is no risk at all, without specific distinction, going beyond intent is asking courts to read your language more specifically than intended.

  2.  Courts will attempt to read different words to have distinct meanings, even if that's a struggle.  By piling on such words, again, you're begging the courts to find more and more narrow slivers of difference where you don't need any.  Also to issue more narrow-reading "gotcha" opinions, prompting more reactive grafting onto already burdensome provisions, to keep the wheel turning.

  3.  Even if you say the general thing you want---no kind of warranty, no kind of damages, no kind of claims---and then offer specific examples with some kind of "including, but not limited to" kludge, you're still showing the court specific examples.  They can't ignore those examples, even if you tell them to, and even if they care to oblige you.  Readers of all kinds will tend to restrict the general class you've described toward the specific examples provided.  Consider ISC:

      > In no event shall ISC be liable for any special, direct, indirect, or consequential damages or any damages whatsoever resulting from loss of use, data or profits...

      Fighting this language out, I'd sure appreciate all that raw, linguistic material just laying around, as opposed to a bare desert of bad news like:

      > In no event shall ISC be liable for any damages whatsoever ...

      At least if there's no background law that requires something akin to legal education by notice.  When that's the case, we often see specific acknowledgments of the statutes in play, affirmative waivers, and notices about having or declining to get legal advice.  That's not happening here.  I've never seen it in a privately executed, countersigned license agreement, either.

  3.  No drafter, anywhere, will come up with every specific legal term of art, for all time, to cover all kinds of warranty, damages, and claims.  That probably isn't even possible, given differences between jurisdictions.  It's like trying to paint a house with disposable markers, in a rainstorm, while the house is being built.

As for what _was_ necessary, I want UCC 2-316(3)(a) "as is" to be rid of implied warranties:

> unless the circumstances indicate otherwise, all implied warranties are excluded by expressions like "as is", "with all faults" or other language which in common understanding calls the buyer's attention to the exclusion of warranties and makes plain that there is no implied warranty

L0-R doesn't have any express warranty language, but just to hammer it home, emphatically, I used "without warranty at all".  Some jurisdictions limit limits of liability, and we don't want a contract-style savings clause taking up space at the end of the license, so "As far as the law allows" will do.  Then the limitation, mentioning "damages", the legal term for what you can get sued to pay out, and "any kind of legal claim", to avoid the trap where courts read contract limitations to exclude only contract claims, unless they say otherwise.

Rather than put all this in `AN IMPENETRABLE, ILLEGIBLE BLOCK OF CAPITAL LETTERS THAT SEEM TO GO ON FOREVER`, I've set it in regular text with some stars.  I've also put it right up at the top.  If that isn't "conspicuous", there's no hope.  Consider the meaning under the Uniform Commercial Code:

> "Conspicuous", with reference to a term, means so written, displayed, or presented that a reasonable person against which it is to operate ought to have noticed it. Whether a term is "conspicuous" or not is a decision for the court. Conspicuous terms include the following: (A) a heading in capitals equal to or greater in size than the surrounding text, or in contrasting type, font, or color to the surrounding text of the same or lesser size; and (B) language in the body of a record or display in larger type than the surrounding text, or in contrasting type, font, or color to the surrounding text of the same size, or set off from surrounding text of the same size by symbols or other marks that call attention to the language.

## Permission

    You may do everything with this software that would
    otherwise infringe copyright in this software, or any patent
    anyone giving this license has or obtains that would have
    read on this software just after any of their contributions,
    on these conditions:

L0-R is structured like MIT, BSD, and their "academic" or "hacker" style progeny, as notices followed by free-flowing paragraphs and numbered conditions.  But unlike those old licenses, L0-R addresses copyright and patent licensing specifically, like Apache 2.0, MPL 2.0, and the other "enterprisey" or "contract" style forms.  I avoided this in initial drafts, by using BSD language.  But no lawyer writing a public software license from scratch today can neglect patent and keep their dignity.

Rather than list out the exclusive rights of copyright holders---reproduce in copies, prepare derivative works, distribute, and so on---L0-R says that you can do all the things with the software that copyright would otherwise stop you from doing.  In other words, all the ways you would "infringe" copyright if you didn't have a license.

Likewise for patent, though with patent, the license needs to go an extra step, and clarify which patents are being licensed.  If you contribute a patch to a project that brings it under a patent you have, or one you get later, you shouldn't be able to turn around and sue users for infringing that patent.  You've laid a trap and sprung it on them.  But if someone else comes along later and contributes a patch bringing the software under still another patent you never intended to license, you shouldn't be stuck licensing it away automatically.  Others shouldn't be able to decide what you have to license.

L0-R is in line with how Apache 2.0 and MPL 2.0 address these issues.  Basically, contributors license patents that cover, or "read on", the project as they contributed to it, with their contributions.

## Conditions

In order to exercise the permission granted by L0-R, you have to meet its conditions.  If you exercise the permission, but don't follow the conditions, you can get sued for infringement.

### Preserve Licensing Information

    1. You must ensure that everyone who gets a copy of this
       software from you, in source code or any other form, also
       gets the complete text of this license and the copyright
       and source notices above.

This is directly analogous to paragraph 2 of MIT, and conditions 1 and 2 of BSD.

Unlike those priors, L0-R requires preserving the notice about source availability, as well.  This is in line with what Apache 2.0 `NOTICE` files often do.

L0-R wants people to have source code.  It helps to tell them where they can get it.

### Patent Termination

    2. You may not make any legal claim against anyone accusing
       this software, or any derivative work based on it, of
       infringing any patent that would read on this software
       alone, without modification or extension.

Licensing lawyers refer to terms like this as "patent termination" provisions.  In essence, if you sue a user of the software for patent infringement, you lose your permission to use the software yourself.  You don't get to benefit from the license, on the one hand, and deny its benefits to others, on the other.

Some open source licenses, like Apache 2.0, terminate just patent permission for suing others under patents.  Other licenses, like GPL 3.0, MPL 2.0, OSL-3.0, and now L0-R, terminate both copyright and patent permission.

Nearly all good open source patent termination provisions use additional language to avoid some bad edge cases.  Hypothetically:

1.  Pat sues Dana for infringing a patent using open source software by Evan.  Evan's software, as he released it, wouldn't infringe Pat's patent.  It's only with Dana's changes that Evan's software infringes Pat's patent.  But Pat loses his permission to use Evan's original software anyway, under the patent termination language of Evan's license, because the license doesn't distinguish suing about Evan's original software, or any modified version of it.

2.  Peter sues Diane for infringing a patent using open source by Errol.  Errol's version infringes Peter's patent, without any changes.  But Dana did make some changes, so the software Peter sues her for using isn't exactly the same as what Errol licensed.  Peter doesn't lose his permission to use Errol's software under the patent termination language of Evan's license, because he isn't accusing Errol's software.  He's accusing Diane's changed software.  The license only terminates his permission for suing about the original software.

L0-R tries to cover these cases correctly as succinctly as possible.

1.  For Pat, L0-R's condition triggers only for a "claim accusing ... of infringing any patent that would read on this software alone, without modification or extension".

2.  For Peter, L0-R's condition triggers on a "claim accusing this software, _or any derivative work based on it_".  "Derivative Work" is a copyright term that links an earlier, "preexisting work" to later work that is "based on" it.  We can use that concept to link modified versions back to the original, to give clarity to this patent provision.

The patent termination provision is the most difficult part of L0-R to read.  I've gone back and forth on how to write the language.  I'm not sure how _simple_ the language can be, since covering these edge cases isn't simple.  But I'd love input on how to improve.

### Sharing Changes

    3. If you modify or extend this software, you must release
       source code for your modification or extension.

Up to this point, L0-R mostly says what other open source licenses said before, in some new way.  Condition 3 says something new.

"Release" is [defined later in the license](#license) to mean, basically, publishing source code as open source.  So L0-R allows modification and extension, as long as you share back.  That makes 3 a "copyleft", "reciprocity", or "share-alike" condition.  It uses the power of copyright, the power to say whether and how others can change copyrighted code, to require that they share their code and give others permission to do so.

L0-R condition 3 differs from existing copyleft implementations in a few ways.

Prior copyleft conditions like GPL, AGPL, and MPL, trigger requirements to share code when you give copies of software with changes to others.  Those licenses use terms like "distribute", "convey", and "modifications" to set up these triggers.

Under the copyright laws, distributing copies is just one of the exclusive rights of copyright holders, just one of the actions copyright holders can sue others for doing without permission.  For example, in the US, the Copyright Act's list of rights also includes making copies and "preparing derivative works", or modifying copies that you have.

L0-R triggers the requirement to share source code on modification alone, not modification and distribution, or modification and making a copy, or modification and any other kind of action.  That means L0-R's trigger fires in more cases than other licenses'.  It requires sharing code in more circumstances, under condition 3 and others that follow.

The open source community puts a lot of value on the ability to modify software.  As it does on the ability to distribute changes.  But it doesn't require those freedoms absolutely.

Every copyleft license puts conditions on some of those valued freedoms.  Because those conditions, on freedoms like copying, running, modifying, and distributing, can actually increase freedom in the community overall.  They help ensure that more people end up with the freedom to work with the software that matters to them.  They stop others from taking software from the community, and passing on less freedom on than what they themselves received.

L0-R asks the question:  Why can't copyleft use _more_ of the power of copyright, more than conditions on distribution with modifications, to require sharing source code and the freedom to work with it?

Proprietary software licenses sure don't limit themselves that way.  Often, when a proprietary software license restricts use to so many concurrent users, or so many installed instances, or running on so many processors, it doesn't say anything at all about which exact exclusive rights of copyright holders are involved.  It's understood, and accepted, that using the software will involve some or maybe all of those rights: distributing to the contractor or platform provider that will run it for you, copying to put it on the machine that will actually run it, modifying to work in a new environment, copying into memory, and so on.  Proprietary software vendors don't want to create loopholes that let customers out of their conditions, based on legal technicalities.  Why should copyleft licenses?

We could answer that question two ways.

On the one hand, we could ask whether we're alright calling a license that uses that kind of legal power an "open source license".  Usually, we think of open source licensing as opting out of legal rules, especially IP rules.  And that's certainly all that many permissive licenses, like MIT, attempt to do.  But licenses that use copyright to protect openness have long been a part of our community, too.

And they've evolved.  More than twenty years ago, the Free Software Foundation and other Free Software advocates faced a challenge.  A challenge that came to be known as the "ASP loophole".  We might call it the "SaaS loophole" today.  Proprietary software developers can take GPL-, MPL-, and other distribution-based copyleft code, modify it, build it into proprietary software, offer that software to customers, and hold their changes back from the community, as long as they run the software for customers over a network, rather than send them copies to run themselves.  Because they aren't distributing copies, copyleft doesn't trigger.

In response, Affero, Inc. and the Free Software Foundation added an additional trigger to GPL, creating the "Affero" series of GPL variants.  AGPL 3.0's additional trigger fires not just on distribution of changed copies, but also on making changed versions available to others over a network.  AGPL doesn't say what exclusive rights under copyright you have to use to make software available that way.  But it doesn't have to.  You will need some kind of copyright permission to do so, that permission comes from AGPL, and AGPL sets conditions you have to follow as a consequence.  AGPL is still an "Open Source" and "Free Software" license, approved by both OSI and FSF.

AGPL is the current benchmark for strong copyleft licenses.  "Strong" in the sense of triggering copyleft conditions in more circumstances than other licenses.  But even AGPL 3.0 leaves open lots of opportunity to take from the open community, build proprietary software, and give nothing back.  Clearly, there's room for copyleft to expand within open source, as did AGPL.  Is AGPL the most copyleft a license can be, and still be an open source license?  If so, why?

On the other hand, we could ask whether driving a harder bargain with users who don't share open values, or who can't live them out in a particular work context, is a good idea.  Even the Free Software Foundation now recommends against using its own copyleft licenses for some kinds of libraries, where others concerns predominate.

In the end, asking how hard a bargain open source should drive with proprietary software makers just isn't that much different from asking what "open source" or "free software" should mean.

So what does open source mean?

### Sharing Incorporating Programs

    4. If you include this software in a larger piece of
       software, you must release any source code for that
       larger piece of software that has not yet been released.


### Sharing Developed Software

    5. If you run this software to analyze, modify, or generate
       software, you must release source code for that software.

## Release

    To release source code, you must license it to the public
    under either these terms or terms approved by the Open
    Source Initiative, and promptly publish it, in the preferred
    form for making modifications, to a freely accessible
    distribution system widely used for similarly licensed
    source code.

## Automatic Forgiveness

    Any unknowing failure to meet condition 3, 4, or 5 is
    excused if you release source code as required within 30
    days of becoming aware of the failure.