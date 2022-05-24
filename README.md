# Dr. Contrast: Or how I learned to stop worrying and love the screenreader

Accessability is easy. So easy in fact that Google Chrome, W3 and Microsoft Windows have fixed the problem for us with blood, sweat and millions of dollars. All we have to do is not go out of way to ruin things. If you follow the standards, listen to the linter and choose sensible color themese we'll all make it out just fine. 

## The Issues 

### Mobility 

This is the easiest category to support. Most users are going to have their own solution worked out for them, mapeed to the standard keys (tab, enter, arrow keys). We just need to make sure we don't break compatability with the standard keys. 

![head_wand_user](https://atprogramnews.typepad.com/.a/6a0120a516ff22970b017c32e8c499970b-320wi)
![alternative_game_pad](https://abilitynet.org.uk/sites/abilitynet.org.uk/files/image30.jpeg)

**Key Considerations:**
* You **must** support tabbing. Or I will fucking murder you. [Just do it](https://www.youtube.com/watch?v=ZXsQAXx_ao0)
* Skip links over skips links.
* Bad forms are obnxious to all users. Simplify and Autocomplete as much as possible
* Timed elements must be pausable. Don't assume users can read that carousel box in .3 seconds. 
* Shortcuts spark joy in everyone.

### Vision

Vision loss is a super broad category. We tend to assume that vision loss is a binary state, either blind or not-blind. This is a bad assumption to make though- the vast majority of people with vision loss or visual impairments are sighted! Think of people who wear glasses, are color-blind, or have other types of eye disease like glaucoma or astigmatism.

**Key Considerations:**
* Use Semantic HTML for screenreaders
* Zooooom your web app and make sure it still works. This is key fallback skill for many
* Use a simulation to check your theme works for color blindness


### Cognitive 

This this the hardest category by far. This is where your designer should shine. Compensating here is all about considering the needs of your users. 

Designing a site for power users will look a lot different than for eldery folks or people with cognitive impairment. What about someone who is new to computers? 

**Key Considerations:**
* Think about your audience. What challenges might they face?
* Usability testing


## The Skills

### Assuming Secret Identities

Learning and utilizing the toolset of disabled users is the gold standard. (Getting actual disabled users to use your stuff is the Platinum Standard). 

#### Screenreaders

Use the built in screenreader for your operating system. If you don't have one, the [tota11y](https://chrome.google.com/webstore/detail/tota11y-plugin-from-khan/oedofneiplgibimfkccchnimiadcmhpe/related?hl=en) has got you covered. 

There are two primary ways that a user will use a screen reaader:
1. Top-to-bottom mode when using reading articles, wikipedia or other long-form text. 
2. Navigation mode for using a web app by cycling through headers, links, and landmarks. 


This is the hardest tool to learn. Don't get discouraged! It's highly reccomended that you _customize_ screenreader to slow down the voice and learn the diff


#### Keyboarding

Many users can't, won't or prefer not to use a mouse. Thankfully coders know how to type. Walk through your user flows using only the standard keys (tab, enter, arrow keys, esc)- notice how annoying it is to have to tab 10+ time through the tab menu? How about that <iframe> that doesn't ever let you exit the modal without reloading the page? 


#### Simulations


### ~Cooking~ The Books

 [Lighthouse](https://developers.google.com/web/tools/lighthouse) is an automated audit tool. There are others like [Dev-Axe Web Tools](https://chrome.google.com/webstore/detail/axe-devtools-web-accessib/lhdoppojpmngadmnindnejefpokejbdd?utm_source=deque.com&utm_medium=referral&utm_campaign=axe-browser-extensions_hero). Like most linters, reading the rule explanations is helpful: [Lighhouse Rule Explanations](https://web.dev/lighthouse-accessibility/#aria)
  
  
You can also conduct audits yourself, like this [A11y Checklist](https://www.a11yproject.com/checklist/) or 

**Pros**
* Fast snapshot
* It's so easy, it's already done
* 80:20 rule. 

**Cons**
* Can't test dynamic elements (think tab focus, :hover color contrast)
* Doesn't catch interactive issues

### OK, Google

There _is_ is an automated tool built for you stack that will do the heavy lifting. These checks are fast, easy to 

**Pros**
* Easy to Use 
* Prevent regressions
* 80:20 rule. 
* Easy to measure over time
* Easy to use in CI

**Cons**
* Easy to ignore
* Can't test dynamic elements (think tab focus, :hover color contrast)


## The Kit

### Browser Extensions

[funky](https://chrome.google.com/webstore/detail/funkify-%E2%80%93-disability-simu/ojcijjdchelkddboickefhnbdpeajdjg?hl=en)

[tota11y](https://chrome.google.com/webstore/detail/tota11y-plugin-from-khan/oedofneiplgibimfkccchnimiadcmhpe/related?hl=en)
  

### Booklearning

## The Stragety Guides
  
  [Microsoft's Mcuh better version of this page:](https://docs.microsoft.com/en-us/microsoft-edge/accessibility/test)
  
 [A11y How-To's](https://www.a11yproject.com/posts/#how-to)
  
 [MDN Learn Accessability](https://developer.mozilla.org/en-US/docs/Web/Accessibility)

### The Standards

This is the official spec. `AA` is the minimum standard, `AAA` is optimal, `A` compliance is asking for a lawsuit. These are hard to read, thankfully 
  
[Web Content Accessability Guidelines](https://www.w3.org/TR/WCAG21/)
