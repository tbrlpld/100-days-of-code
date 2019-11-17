# 100 Days Of Code - Log


## Day 1: October 16, 2019, Wednesday

### Today's Progress
Gone through first bit of Flask introduction and set up the basic project structure in #100DayOfWebInPython.
Also, enabled Markdown formatting for posts in the Flaskr blog app (as suggested in the "Keep Developing" section of the Flask tutorial).

### Thoughts
Have used Flask before, but the `.flaskenv` file using `python-dotenv` package to set the environment variable automatically is a nice addition to simplify the setup (and distribution I guess).
`markupsafe.escape()` can be used to sanitize user input on the sever side. 


### Link(s) to work
1. [#100DayOfWeb in Python -- Intro to Flask](https://github.com/tbrlpld/100daysofweb-with-python-course/tree/master/days/001-004-flask-intro)
2. [Flask tutorial -- Keep Developing](https://flask.palletsprojects.com/en/1.1.x/tutorial/next/)
3. [Day 1 Commit](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/264b84806a7cf0b0268107a74ff8c9fa64ac6513)

## Day 2: October 17, 2019, Thursday

### Today's Progress
Started the day off with the rest of the Flask intro lessons on #100DayOfWeb in Python. 
Added templates, base template, and some MUICSS for styling and page consistency.

### Thoughts
Using `.html.j2` as the file extension for the Jinja2 templates makes SublimeText show them with correct syntax highlighting. 

### Link(s) to work
1. [#100DayOfWeb in Python -- Intro to Flask](https://github.com/tbrlpld/100daysofweb-with-python-course/tree/master/days/001-004-flask-intro)
2. [Day 2 Commit](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/6be58f42cae9dad32b9fb1f41709efed0c6f625f)


## Day 3: October 18, 2019, Friday

### Today's Progress
Started new Flask site from scratch. 
Site pulls Markdown files from my #100DaysOfCode journal repo on GitHub and renders them into a base template.
Styling of the page with MUICSS is still open.

### Thoughts 
In a Jinja base template, you can access a child template’s blocks not only by `{% block content %}{% endblock %}` but also via the special `self` object. 
To access the child's block use `{{ self.content() }}` in the parent/base template. 


### Link(s) to work
1. [#100DayOfWebInPython -- Intro to Flask](https://github.com/tbrlpld/100daysofweb-with-python-course/tree/master/days/001-004-flask-intro)
2. [Day 3 Commit](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/6733101af90e50f34d8aa8e5cdff736b92af44c0)


## Day 4: October 19, 2019, Saturday

### Today's Progress
Applied some style to my Flask journal app with MUICSS. 
Also, I added the Flask journal app to [my personal website](https://lpld.io) 😊

### Thoughts
The documentation of MUICSS and the features all seem a little less polished then the Bootstrap competition.
Especially the concept of `mui-appbar` is not quite clear, because there is no example on how to combine it with other elements.

Figuring out how to deploy the Flask app on my website took actually the most time. 
Couldn't figure out how to do it via unix socket as it was suggested on [Digital Ocean](https://www.digitalocean.com/community/tutorials/how-to-serve-flask-applications-with-gunicorn-and-nginx-on-ubuntu-18-04#step-4-%E2%80%94-configuring-gunicorn) . 
So now I am running the Gunicorn server and proxying from Nginx to it.

### Link(s) to work

1. [#100DayOfWebInPython -- Intro to Flask](https://github.com/tbrlpld/100daysofweb-with-python-course/tree/master/days/001-004-flask-intro)
2. [Day 4 Commit](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/a05bb14a112ed98d10be758b3c5a8bca4dc17635)
3. [Live Version of 100 Day Journal](https://log100days.lpld.io/)


## Day 5: October 20, 2019, Sunday

### Today's Progress
Today no planned activity in #100DaysOfWeb course today, only video. 

To still code a bit, I continued Flask tutorials "Keep Developing" section by implementing an RSS Feed for new posts.  
This should be interesting, because I really never never worked with RSS. 
Neither on client nor server side. 

This concludes the proposed topics in the Flask tutorial "Keep Developing" section. 

### Thoughts
RSS seems pretty simple. Just an `.xml` file that is regularly polled by an interested reader.
But, is anybody still using RSS (as a user)?

### Link(s) to work

1. [#100DayOfWebInPython -- HTML & HTML 5](https://github.com/tbrlpld/100daysofweb-with-python-course/tree/master/days/005-008-html5)
2. [Flask tutorial -- Keep Developing](https://flask.palletsprojects.com/en/1.1.x/tutorial/next/)
3. [Day 5 Commit (to Flask tutorial)](https://github.com/tbrlpld/flask-tutorial/commit/703d5e2f67f62c3a23884d1b5adb3226e9381b6d)


## Day 6: October 21, 2019, Monday

### Today's Progress
Recreated the Google landing page from 1998 with HTML. 

### Thoughts
Client side form input validation is pretty helpful, because it is immediate.
It doesn't replace server side validation, but is helpful in it's responsiveness. 

### Link(s) to work

1. [#100DayOfWebInPython -- HTML & HTML 5](https://github.com/tbrlpld/100daysofweb-with-python-course/tree/master/days/005-008-html5)
2. [Day 6 Commit](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/52fec0b1b494fdc778887c0945ac4e9b550d7079)


## Day 7: October 22, 2019, Tuesday

### Today's Progress
Made the recreated 1998 Google landing page responsive 😊

### Thoughts
Images create a strange space below it. No padding or margin set. This can be removed when setting `display` to `block`.


### Link(s) to work

1. [#100DayOfWebInPython -- HTML & HTML 5](https://github.com/tbrlpld/100daysofweb-with-python-course/tree/master/days/005-008-html5)
2. [Day 7 Commit](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/c52e66090af552e959d524fee3eed996ad4acb98)


## Day 8: October 23, 2019, Wednesday

### Today's Progress
Spent a bunch of time trying to contribute to `wemake-python-styleguide` to add a clarification in the documentation. #Hacktoberfest

Created register form for responsive 1998 Google landing page for #100DaysOfCode. 

### Thoughts
`flake8` was running slow an throws a bunch of warnings in `wemake-python-styleguide`. 
Not sure if this is normal or caused by my setup. 

Working on a linter, that uses several linters and linting packages and also lints itself if kind of a brain fuck 😬

### Link(s) to work

1. [wemake-python-styleguide Pull Request](https://github.com/wemake-services/wemake-python-styleguide/pull/936)
2. [#100DayOfWebInPython -- HTML & HTML 5](https://github.com/tbrlpld/100daysofweb-with-python-course/tree/master/days/005-008-html5)
3. [Day 8 Commit -- #100DaysOfWeb](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/7d0bcbe74b108180b8c242c21eb81a4e5b70eea2)


## Day 9: October 24, 2019, Thursday

### Today's Progress
Learned basics of API Star and Postman #100DaysOfWeb @TalkPython @Pybites.
Implemented cars API with read all, read one and create new car endpoints.


### Thoughts
The API Star version used (0.5) seems outdated and the package has been massively remodelled in its following release (0.6).

### Link(s) to work

1. [#100DayOfWebInPython -- API Star](https://github.com/talkpython/100daysofweb-with-python-course/tree/master/days/009-012-modern-apis-starred)
2. [Day 9 Commit -- #100DaysOfWeb](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/dd1d42b11b71e7ce716946b8180ca31174c0e9a9)


## Day 10: October 25, 2019, Friday

### Today's Progress
Continued learning about API Star and testing with `pytest. 
Extended the car API with update and delete features and added testing for all endpoints. #100DaysOfWeb @TalkPython @Pybites

### Thoughts
I do like the simplicity of `pytest` alot! Better than the class definition used by `unittest`.

No idea what kind of API to build in the next two days so far.

### Link(s) to work
1. [#100DayOfWebInPython -- API Star](https://github.com/talkpython/100daysofweb-with-python-course/tree/master/days/009-012-modern-apis-starred)
2. [Day 10 Commit -- #100DaysOfWeb](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/5012fd29a38cb7d0963013b5c3e5aa43ab797b21)


## Day 11: October 26, 2019, Saturday

### Today's Progress
Started creation of simple users API with API star for #100DaysOfWeb @TalkPython @Pybites
Applied TDD by writing the functions with `pytest` first.
Read for all and one is implemented. Next is Create, Update and Delete.

### Thoughts
The change in API Star resulted in them overhauling the documentation. 
Could not find the documentation for 0.5 anymore.

### Link(s) to work
1. [#100DayOfWebInPython -- API Star](https://github.com/talkpython/100daysofweb-with-python-course/tree/master/days/009-012-modern-apis-starred)
2. [Day 11 Commit -- #100DaysOfWeb](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/f4f615ba52e7da80f945cf1526c3dd9388913d73)


## Day 12: October 27, 2019, Sunday

### Today's Progress
Continued users API with API star for #100DaysOfWeb @TalkPython @Pybites
Added create, update and delete endpoints in test driven manner.

### Thoughts
This was fairly routine by the second time.
I would probably be more complex when there are more features included or checks that need to be performed.
Does it make sense to create a bunch of CRUD endpoints that are only used internally in an application? 

Today was also a travel day. Worked on the programming quite late, so I could not really give it my best.

### Link(s) to work
1. [#100DayOfWebInPython -- API Star](https://github.com/talkpython/100daysofweb-with-python-course/tree/master/days/009-012-modern-apis-starred)
2. [Day 12 Commit -- #100DaysOfWeb](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/03adf2b642c961e64b77f25786c87805fb9eb0c6)


## Day 13: October 28, 2019, Monday

### Today's Progress
Learned some CSS basics from #100DaysOfWeb @TalkPython @Pybites
Finally getting a grasp on the CSS selector chaining and inheritance.

Also, tried to get back into an old [Django project of mine](https://gitlab.com/tbrlpld/caejobdiary).
Mainly reading old code. Trying to get back into the structure.

### Thoughts
No code created today. Mainly occupied with reading code.
Does not feel good, but I guess it is understandable that it takes some time trying to get back into an old project that I have not touched for months.

### Link(s) to work
1. [#100DayOfWebInPython -- CSS Basics](https://github.com/tbrlpld/100daysofweb-with-python-course/tree/master/days/013-016-css-basics)


## Day 14: October 29, 2019, Tuesday

### Today's Progress
Played around with CSS selectors a bit #100DaysOfWeb @TalkPython @Pybites

Continued with my old Django project. 
Struggling to find a good solution for a may-to-many widget.

### Thoughts
Really wondering if I should create the the many-to-many solution myself or trying to make it work with `django-autocomplete-light` (DAL). 
My issues with it are that it does not validate the tags and also does not enforce the uniqueness. These are typical Django issues when using the `.save()` or `.get_or_create()` method of a model.

Also, I do not know how to render it in my custom form. 
Guess I could just copy and paste the rendered from and make my modifications. 

Another day without any meaningful progress. 
This really sucks now. 
Guess this is why I abandoned that project before...

### Link(s) to work
1. [#100DayOfWebInPython -- CSS Basics](https://github.com/tbrlpld/100daysofweb-with-python-course/tree/master/days/013-016-css-basics)


## Day 15: October 30, 2019, Wednesday

### Today's Progress
Recreated talkpython.fm header from a list using CSS #100DaysOfWeb @TalkPython @Pybites

The vertical alignment of the image was especially tricky. 
You need to define an element before that like this:
    
    .frame:before {
        content: "";
        display: inline-block; 
        vertical-align: middle;
        height: 100%;
    }


### Thoughts
CSS has a bunch of weird side effects that are not always very clear.
This is where front-end frameworks really help.

### Link(s) to work
1. [#100DayOfWebInPython -- CSS Basics](https://github.com/tbrlpld/100daysofweb-with-python-course/tree/master/days/013-016-css-basics)
2. [Day 15 Commit -- #100DaysOfWeb](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/57dc34280b6a02c210fef6819737837b97c30461)


## Day 16: October 31, 2019, Thursday

### Today's Progress
Learned about Python type hinting and mypy. 
Worked on the "change" kata using OOP and created a single executable with PyInstaller .

Also, checked out a few bootstrap templates for #100DaysOfWeb @TalkPython @Pybites

### Thoughts
Guess this was the first time actually using OOP in the proper manner.
Also the first time I made a single executable of an app! Super easy with PyInstaller! 
That is awesome.


### Link(s) to work
1. [#100DayOfWebInPython -- CSS Basics](https://github.com/tbrlpld/100daysofweb-with-python-course/tree/master/days/013-016-css-basics)
2. [Day 16 Commit -- "Change" Kata](https://github.com/tbrlpld/kata/commit/29aefb720d3b18ec406c48dcfd88e09982713282)


## Day 17: November 1, 2019, Friday

### Today's Progress
Learned about how to combine Flask and Requests to display data from APIs.
Create a page to display random Chuck Norris jokes for #100DaysOfWeb @TalkPython @Pybites using https://api.chucknorris.io/

### Thoughts
Really like how simple it is to grap data with requests.


### Link(s) to work
1. [Day 17 Commit -- #100DaysOfWeb In Python](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/6edd73912c5d0e2f6e73a9e967bd53d01e2f9a70)


## Off-Day: November 2, 2019, Saturday

Attended friends' wedding.


## Day 18: November 3, 2019, Sunday

### Today's Progress
Created a page to display beers 🍺 sorted by their IBU value with brewerydb.com for #100DaysOfWeb @TalkPython @PyBites

### Thoughts
It is kind of crazy how many endpoints for brewerydb.com exist. 
Well, I guess thats because they make this a business. 

Also, there is an app by them called BreweryMap, which does exactly what it says 😊🍺


### Link(s) to work
1. [Day 18 Commit -- #100DaysOfWeb In Python](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/5b819564bf6198e51bc9bda98eae7a11a7159b56)


## Day 19: November 4, 2019, Monday

### Today's Progress
Learned how to combine Flask form actions and API calls and created a page to display Pokemon by a given color for #100DaysOfWeb @TalkPython @PyBites

### Thoughts
This was fairly simple. I really like how straight forward Flask is. 

Also, project idea: APIAPI ^^

### Link(s) to work
1. [Day 19 Commit -- #100DaysOfWeb In Python](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/bdb517723d85735db330adffb980dd273d8b0740)


## Day 20: November 5, 2019, Tuesday

### Today's Progress
Tried to extend the Pokemon page with additional information for #100DaysOfWeb @TalkPython @PyBites
This resulted in a very slow implementation, because each Pokemon's endpoint needs to be hit separately to get more data. 

### Thoughts
The PokeAPI can get a little confusing, because the different values are not really explained. 
E.g. what is a Form or Nature of a Pokemon, how a certain Pokemon is the combination of Form and Species, etc. 
This makes it a little confusing to work with.  

The design of the API requires to first get the species of a color and get every species to extract every color.
This is not very performant.

### Link(s) to work
1. [Day 20 Commit -- #100DaysOfWeb In Python](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/c021246b19cf0dcbc7d3d3fa8b2e189963928842)


## Day 21: November 6, 2019, Wednesday

### Today's Progress
Learned about `asyncio` and turned a simple python script from sync to async #100DaysOfWeb @TalkPython @PyBites
This is my first contact with asynchronous programming.

### Thoughts
This is really complex. 
Main use case for async is to let the current thread do other work, while it is waiting for the reponse of an outside resource.

### Link(s) to work
1. [Day 21 Commit -- #100DaysOfWeb In Python](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/e6a8581656a2161a78a87ba39c987fcf2cd44b66)


## Day 22: November 7, 2019, Thursday

### Today's Progress
Turned an existing synchronous web scraping script into an async one #100DaysOfWeb @TalkPython @PyBites


### Thoughts
It is still tricky to find out where to add the asynchronous functions.

### Link(s) to work
1. [Day 22 Commit -- #100DaysOfWeb In Python](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/b7a611899898876335af7dbe5560fd126468548a)


## Day 23: November 8, 2019, Friday

### Today's Progress
Learned how to turn a synchronous #pythonflask API app into an asynchronous Quart app #100DaysOfWeb @TalkPython @PyBites
Used learned skill on two endpoints of a predefined Flask app ✅

### Thoughts
I guess the place to add the async functions is anywhere where an external service is slow. 
This could be a database interaction or web request. 

Minor hickups due to wifi blacking out and me wondering if my web calls are bad ^^. 
Also, internet (cellular) is particularly slow today. 
Can't wait for the cable connection.

### Link(s) to work
1. [Day 23 Commit -- #100DaysOfWeb In Python](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/505d3e156089440d36955a75f5282462983bee9e)


## Day 24: November 9, 2019, Saturday

### Today's Progress
Turned my `log100days` app, which renders my markdown log into HTML, from Flask to an async Quart app. 
Because I am not caching any of the markdown in the app, this should really increase performance and scalability. 
 #100DaysOfWeb @TalkPython @PyBites


### Thoughts
Internet is way too bad... can't deploy the app right now...
Damn. Developed the Quart app with a newer version of Python than I have on the server...
So this did not work. 
Now I need to update the Python on the server. But for some reason on the server there are not all tools I need! 
How to get `zlib` on Ubuntu? 

Looks like you need a bunch of packages to install Python on Ubuntu. 
[Here are some listed](https://askubuntu.com/questions/21547/what-are-the-packages-libraries-i-should-install-before-compiling-python-from-so)

```
build-essential
libncursesw5-dev
libreadline-gplv2-dev
libssl-dev
libgdbm-dev
libc6-dev
libsqlite3-dev
libbz2-dev
libffi-dev
liblzma-dev
tk-dev
libdb-dev
```

This finally worked. 
Damn this took me most the time today. 
Ok, the slow connection to my server also did not make it any faster.

**But** this points out why development environment and deployment environment should always be as similar as possible‼️

### Link(s) to work
1. [Day 24 Commit -- #100DaysOfWeb In Python](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/d1f4557f278e2d10a2f5e7c76e4d59020928c972)


## Day 25: November 10, 2019, Sunday

### Today's Progress
Learned JS basics from #100DaysOfWeb @TalkPython @PyBites

Also, dove into object-oriented JS with @MozDevNet

### Thoughts
Glad there is finally a `class` syntax in ECMAScript2015!

JS is so implicit 😏 and I really support Python's "Explicit is better than implicit." 

Really need to get used to this. 
Seems like as JS is getting better, it is getting more and more similar to Python 🙃

### Link(s) to work
1. [Day 25 Commit -- #100DaysOfWeb In Python](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/d9cf4682e0c3f6a6fda79fcc802245aafd123644)
2. [Inheritance in JavaScript -- MDN](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Inheritance)


## Day 26: November 11, 2019, Monday

### Today's Progress
Practised JS basics with four little exercises for #100DaysOfWeb @TalkPython @PyBites


### Thoughts
The basics of JS seem quite simple and similar to Python.

### Link(s) to work
1. [Day 26 Commit -- #100DaysOfWeb In Python](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/f18961caa478ebc572e2e2f5c8a92a6bf3ecc57d)


## Day 27: November 12, 2019, Tuesday

### Today's Progress
Learned about and played around with vanilla #JS DOM manipulation #100DaysOfWeb @TalkPython @PyBites

### Thoughts
Never done DOM manipulation without jQuery so far ^^ 
Good to know how to do it without any external dependencies.


### Link(s) to work
1. [Day 27 Commit -- #100DaysOfWeb In Python](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/aa553e8c42fe55535b279708bf814e00004134c9)


## Day 28: November 13, 2019, Wednesday

### Today's Progress
Practised #JS by implementing a simple calculator and a calorie counting app #100DaysOfWeb @TalkPython @PyBites

<!-- ### Thoughts -->


### Link(s) to work
1. [Day 28 Commit -- #100DaysOfWeb In Python](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/2f6f14a6dea7c7523e5954c6b457e94baca65452)


## Day 29: November 14, 2019, Thursday

### Today's Progress
Learned about static site generation with @getpelican, @GitHub and @Netlify #100DaysOfWeb @TalkPython @PyBites

Went overboard and watched all videos for two days and put the new knowledge to work.
So, I have a blog now ^^ blog.lpld.io

### Thoughts
Nice. 
I wanted to create a blog for myself anyhow. 
Now I got one through this source 😅 

### Link(s) to work
1. [Day 29 Commit -- #100DaysOfWeb In Python](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/80e795481ecaa6e8a3e606f1c9b2f79e72b5eb04)


## Day 30: November 15, 2019, Friday

### Today's Progress
Started contributing to @getpelican to make the default template responsive.
 #100DaysOfWeb @TalkPython @PyBites

### Thoughts
Most of my time when in to get my setup running though 😅 
Hope to be more productive tomorrow.

### Link(s) to work
1. [Day 30 -- Pelican Contribution Branch](https://github.com/tbrlpld/pelican/tree/add-mcss-grid)
2. [Pelican Issue -- Responsive Base Template](https://github.com/getpelican/pelican/issues/1704)


## Day 31: November 16, 2019, Saturday

### Today's Progress
Continues making the @getpelican default template responsive.
So mainly css today.
 #100DaysOfWeb @TalkPython @PyBites

### Thoughts
Wow, this is taking quite some time.

### Link(s) to work
1. [Day 31 -- Pelican Contribution Branch](https://github.com/tbrlpld/pelican/tree/add-mcss-grid)
2. [Pelican Issue -- Responsive Base Template](https://github.com/getpelican/pelican/issues/1704)
