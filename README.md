# Neighborhood Spots Map

Tonight we'll be building a map of your favorite neighborhood spots around Los Angeles. See the live version here: http://machikoyasuda.github.io/los-angeles-map/

It's pretty lonely at the moment. We need you to help contribute a spot to the map! To do this we'll show you how to create a GitHub pull request with your haikus.

## Setup

Before we start, make sure you have:
 - **A GitHub account**
 - **Install Git**
 - **Install a text editor.**

## Exercise

Depending on whether you're using the command line tools or the GUI, some of these steps will be different.

### Clone

The first step is to copy down our repository. This is called cloning.

If you are using the git command line, first open a terminal. Then decide where you want to keep our project files. If you don't know, try running this in your terminal:

```sh
git clone https://github.com/machikoyasuda/los-angeles-map.git
```

You should now be able to run a local version of our neighborhood app.

In your terminal change to our *project directory* (this is the folder you just cloned).

```sh
cd los-angeles-map
```

Then use `http-server` to start a local webserver:

```js
http-server
```

Now open a browser and go to `http://127.0.0.1:8080/`. You should see our  map. If not, or if you see some kind of error, there was a problem with setup somewhere. Let us know, and we'll help you figure it out!

To quit the local webserver, in the terminal type CTRL+C.

### Contribute

The first thing to do when making changes to a project, is to create a new branch. What **is** a branch anyway?

Remember we're writing **place** haikus. So think about the place you want to write about, and create a branch named after that place.

Since your other terminal is busy serving our website, you'll need a new one. Open another terminal and go to our project directory.

```sh
cd ~/los-angeles-map
git checkout -b echo-park-lake-haiku
```

Then open your text editor and use it to open the `spots.csv` file in our project directory.

Now, come up with a haiku about your place.

**This is the hard part.** Traditional Japanese Haiku are "short poems about a fleeting moment in nature" with no specific syllabic constraints. Less traditionally, American haiku's tend to follow a rigid three line "5-7-5" syllable format and tend to be about whatever. Either way, don't fret too much. Any issues with your haiku will be addressed in our forthcoming rigorous *haiku pull request* process. :wink:

**This is the easy part.** We'll need the latitude and longitude of your place to be able to plot it on the map. There are lots of ways to find lat/lon. Try this on: http://itouchmap.com/latlong.html

Once you've decided on a place, found it's lat/lon, and come up with a haiku, enter it into the haiku.csv in a similar format to the existing haiku.

```
github,haiku,latitude,longitude
"michaelkirk","Illicit lotus<br />Chili mango, jicama<br />This lake has secrets.",34.073,-118.261
```

**Note** put your haiku in quotes, and separate the lines with a `<br />` html tag.

### Commit

Committing is how you "snapshot" your changes to git.

If you are using command line git, from your project directory run this:

```sh
git add spots.csv
git commit -m "Added my haiku"
```

You can check that it worked by running "git show" in your terminal. You should see some output in your terminal which includes your new haiku.

### Push

So at this point your haiku changes are only in your local git repository. But the goal is to contribute your local work back to the main repository so everyone can appreciate it at http://maptimela.github.io/neighborhoods.

If you are using command line git, from your project directory run this:

```sh
git push origin echo-park-lake-haiku
```
**Remember** to substitute in whatever your branch name was for "echo-park-lake-haiku"!

If this worked you should be able to see your branch on github by going to: https://github.com/machikoyasuda/los-angeles-map/branches

### Pull request

What's a pull request?

To create a pull requets...

 - Go to https://github.com/machikoyasuda/los-angeles-map
 - Go to "Pull requests" and then "Create"
 - Leave the base branch as "gh-pages" but change the "compare" branch to your branch name.

Don't see it? Then likely there was an issue with the [push](#push) step. Try again or ask for some help!

At this point, your pull request is waiting to be merged back into the main project. Try to find a nice reviewer for feedback on your haiku and it will get merged in no time!

If you see an error about *merge conflicts*, ask for help!
