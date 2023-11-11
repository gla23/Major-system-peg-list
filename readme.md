A test of [Directus](https://directus.io/) to create a DB of TV/film characters to help create an amazing major system peg list.

# Purpose

The idea goes like this:
- Write out all the characters I can think of that have great mnemonic strength for me personally.
- List potential aliases and the major system digits they convert to.
- Fit the characters into a `00` - `99` peg list. Find alternate names for great characters for which there is a major number clash, or that don't have a 2 digit number. Sometimes it's worth being creative with the aliases to be able to use a great image. Character aliases could be:
  - Character first name
  - Character surname
  - Actor firename
  - Actor surname
  - A character quality or nickname
- If there are still missing slots, systematically work through the TV shows/Films (sources) already used for other charaters that will likely have good images.
- If there are still missing slots after this, look at the full sources list to think of other similar shows I've forgotten about that will likely have good images.

# How to use
The setup is very simple:
1. Clone repository with `git clone https://github.com/gla23/Major-system-peg-list.git major-system`
1. Install Docker
1. Start the container with `docker compose up -d`
1. Login to localhost:8055 (it takes a little while for the container to fully start up the first time), using the admin details in `docker-compose.yml`