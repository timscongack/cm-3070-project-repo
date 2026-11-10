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



## (31 Oct 2026)

After some time off I realized the the idea of a software factory is one that's pretty well covered by eexisting products, but more importantly it doesn't fit the multi modal model approch needed for this project. 

I've been experimenting with building learning apps/study tools, and have been experiencing in the workplace, and witness/conversing with others about their the feelings of inadequacy/lack of knowledge working with very smart people or how AI highlights lack of knowledge. Also, it's hard to keep up with knowledge/build an identity as a learner, and most importantly not trick yourself that you've learned things with LLMs so readily available.

I've decided to continue with idea 4.1 but build an app that assess affect around not knowing then developers lesson plans to actually close the knowledge gaps. 


- wrote the specification, and text for presentation based on week 3 outline
- built the imposter gym walkthrough for the pitch video using claude
- first card names the template: CM3020 AI, idea 4.1
- iterated written components of presentation a few times, and ran recording about 6 times kept going over need to cut out parts but submitted a initial proposal in week 3

## (2 Nov 2026)

- watched the lectures, clear the presentation on proposal needs to be tighened and added to 
- citations for imposter syndrome: Clance & Imes 1978, Sakulku & Alexander 2011, Bravata 2020 (9-82% across studies). recent surveys 43-64% (Hays, MyPerfectResume)
- NO evidence its increasing - so I'm not going to claim that in the presentation
- users = anyone who feels it. student, new grad, working professional
- I need to add what the features/workflow of the app is basically it is mood check > lesson > recall (type or talk) > return at 1 + 7 days > record > app steps back
- gym: need > feature board, research question on the exit card, tracker row, users + evidence on locker card
- rewrote script to tighen and actually keep me on track in the presentation instead of just trying to speed up talking.

#### What I'm doing:

TLDR: Imposter Syndrome Fix

1. Template: CM3020 AI, idea 4.1: orchestrate AI models to achieve a goal.
2. Problem: fix people's "imposter syndrome". It is a learning app, not a therapy app but adjust on feelings
3. Users: anyone who encounters knowledge gaps or feels like an imposter 
4. Evidence: Meta analysis studies range from 9% to 82% have it (Bravata 2020), and recent workplace surveys put it at 43-64%. I found no evidence it is increasing.
5. The need: people brush the feeling off instead of closing the knowledge gap. Maybe do a lookup and forget, then repeat the cycle. They never build an identity as someone knowledgeable.
6. What the app does: it helps you act on the feeling, close the gap, and build a learner identity without becoming a crutch.
7. Why AI: we  need to not only dynamically create learning material but also adjust workload/task on mood/affect
8. Prior work: a notebook with a plain chatbot like Claude, Anki, Oboe, Duolingo and scroll feeds more or less does this but learning tool don't really have affect adjustment 
9. Flow: user describes feeling, and situation, a short lesson with a checked visual aid, then recall by typing or talking. You return at 1 and 7 days, and the app steps back over time.
10. Models: a therapist (emotion classifier), a coach (text LLM), a doctor (vision model) and a teacher  (+ text-to-speech and speech-to-text fr the interactive component).
12. Sidecar: another agent reads the logs and proposes improvements, and I approve them.
13. Engagement: it turns the scroll and dopamine pull into active recall. It borrows Duolingo-style interactive conversation.
14. Question: does mood-adapted active recall beat a plain chatbot on recall after 7 days and on learner identity? The study uses 8-10 people over 2 weeks.

## (Nov 10 2026)

- Premise review, read literature on understanding what imposter syndrome and it's other types, and what are the best treatment methodlogies.

- want to see RCTs/other clinical research on what works/does not

- methods and techniques 
- review of all model types and candidate models
- literature and best practices on model evaluation 
- adversarial models in production
- general design pattern of the application

