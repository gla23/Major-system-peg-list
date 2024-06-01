A [Directus](https://directus.io/) app for creating a database of TV or film characters, in order to build an amazing major system peg list.

# Purpose

Creating a large peg list of strong mnemonic images is hard. You not only need to find many strong images that work for you personally, but also map them into the `00`-`99` slots with a meaningful link.

I created this app to help with these two tasks.

While building a peg list over a couple of years, I started to understand what makes a mnemonic image weak or strong. Lots of the images I had chosen for my list were weak, even after thinking they were strong initially!
I realised my goal of having 100 strong images would be impossible without a tool to sytematically work through all the leads I could think of and catalog any inspiration I had over time.

Here are some of the issues I was facing:

- It was impossible to think of strong images on the spot.
- I was working up from `00` and sometimes had to settle with an image that wasn't great, due to lack of alternatives.
- I sometimes chose a character thinking it was a good image but later realised it wasn't great. For example:
  - I can't visualise Nemo walking or doing many other actions
  - I can't visualise Darth Vader's facial expressions!
- I found myself thinking through the same films over and over again. I often discounted their good images as their name didn't map into the `00`-`99` list.

These problems were solved using the app:

- Storing the characters by their source (e.g. film) allowed me to think through any characters I had missed. I still record the bad ones and rate them with a low star so I don't go over them again.
- The list of sources can be used to brainstorm other sources that would have good chracters.
- I realised the link could be something other than the character's name. The app stores different major names that could be used for each image. This gives me the ability to go back and revisit previous decisions e.g. move a chracter into another slot that's free. I can also record the good characters (rate them 5 star) and later come up with a creative link to fit them in a hard-to-fill slot.

There is also an HTML file that uses the Directus API to display the current progress of your list. It also shows how your characters can be mapped onto a playing card and uno deck. The free characters are dumped at the bottom to help fill missing slots.

# Process

My process was something like this:

- Record all the characters I can think of:
  - Systematically work through the TV show and film list (sources), finding all the characters I can.
  - Look at the sources list to think of other similar shows/films I've forgotten about that will likely also have good images.
- Rate the mnemonic strength of each character for me personally. Be brutal with images I'm not sure about - it's better to have no image than realise it's a weak one after you've memorised the link.
- List potential aliases (and the major system digits they convert to) for the strong characters. Mark the best one as "in use" if the slot is empty. It's worth being creative with the aliases to be able to use a great image that would otherwise not fit in the list. Character aliases could be:
  - Character first name (e.g. Sam for Samwise Gamgee)
  - Character surname (e.g. Solo for Hans Solo)
  - Actor first name (e.g. Katie for Morgana)
  - Actor surname (e.g. Elba for Heimdall)
  - A sound or catch phrase (e.g. [Mhmmm for Yoda](https://www.youtube.com/watch?v=s3_Ojtvr6dM) and [Mope for Chewbacca](https://www.youtube.com/watch?v=5HZHcUaQMF0)!)
  - A character quality or nickname (e.g. Chill for Frozone)
- Repeat the above until stuck. For me it was tricky to fill the last few spots!
  - When lacking strong images, go back to step one.
  - When 4 or 5 star images don't fit into a slot, try to come up with more aliases.
  - Finally one last tactic to fill a nasty slot (Oh `89`!) is to use a major system word generator like Numzi. It may be that one of the words provided could be used as a link to one of your the free characters.

# Plans

Ideas to do:

- Create a bookmark for un-used 4-5 star characters once [https://github.com/directus/directus/issues/19890](#19890) has been addressed. Currently the HTML file displays these at the bottom.
- Add the ability to quickly remove a whole film from your list (e.g. someone who forks the project hasn't seen that film and isn't interested in the characters)
- Use the kanban layout to allow others to easily update the character ratings for them
- Experiment with a custom page within the Directus app to copy the behaviour of the HTML file:
  - Display the curernt list, highlighting any weak characters
  - Show the playing card and uno deck mappings

# How to use

It's very simple:

1. Clone repository with `git clone https://github.com/gla23/Major-system-peg-list.git major`
1. Install Docker
1. Start the container with `docker compose up -d`
1. Login to localhost:8055 using the admin details in `docker-compose.yml`. It takes a little while for the container to fully start up the first time.
