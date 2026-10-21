## Topic 1 Project Concept:

todo:

- [] Choose a project template
- [] Background research
- [] Concept Pitch (peer review)
  - [] 3-5 min video
  - [] display knowledge of the topic and previous works
  - [] critically evaluated the previous works; making judgements
  - [] should cover gap areas or use techniques proven effective
  - [] is project justified given the domain and users?
- [] Need to outline aims, but also log the thinking behind these as this will have to be revisied
- [] Document all decisions, and thinking behind all the decisions throughout the process
- [] Choose something interesting; need to really think about what I like and what I want to do for 6 months
- [] Ask tutors questions, help and show what I'm working on get feedback

## Project Templates I find interesting:

 - 13.1 Project Idea 1: Gamified Smart Environment to Promote Mental and Physical well-being in our Everyday Life
 - 13.2 Project Idea 2: Multi-human Detection and Activities Tracking in a Shared Space
 - 3.1 Project Idea 1: Neural Style Transfer
 - 3.2 Project Idea 2: Deep Learning Breast Cancer Detection
 - 4.1 Project Idea 1: Orchestrating AI models to achieve a goal
 - 4.2 Project Idea 2: Financial Advisor Bot

## (21 Oct 2026)

Going with 4.1, orchestrating AI models. The other ideas felt either too easy or too hard to get a decent result from in 20 weeks.

Idea: a small "software factory". Agents take a text spec and build a small React app (one page to start with). I'm keeping it small, but I'd like it to also provision infra. 

Three models, three kinds of data:
- LLM for spec to code and for fixing bugs
- image-to-text model to look at a screenshot of the running app
- a classifier to say what kind of UI problem it is, or whether the UI matches the spec

What I need to build for that:
- a set of screenshots where I know what's wrong (overlapping text, bad contrast, missing button)
- for each model: how often it's right, how often it makes things up, how slow, how much it costs
- try a few candidates, keep the ones I reject and say why
- check if one multimodal LLM can do the job of the separate models. If I still use separate ones I need to explain why.
- baseline: one plain LLM prompt vs the whole factory. If the factory doesn't win, say so.

- can an image model actually judge a UI?
- agents writing weak tests so their own code always passes
- does the build / check / fix loop settle down or just go round in circles?
- does the app do what the spec asked, not just run?
- I sort of need to build an whole model evaluation framework here; maybe do a framework that evaluates models.

Still to check:
- ask tutor if I can use a CM3020 template (this is CM3070, I think any template is fine, but not sure)
- the PDF is from April 2025 and some of its models are old (BLIP, MobileNet, YAMNet). Check they still work before I rely on them.
- API costs don't want costs to explode
- 
