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
Continued making the @getpelican default template responsive.
So mainly css today.
 #100DaysOfWeb @TalkPython @PyBites

### Thoughts
Wow, this is taking quite some time.

### Link(s) to work
1. [Day 31 -- Pelican Contribution Branch](https://github.com/tbrlpld/pelican/tree/add-mcss-grid)
2. [Pelican Issue -- Responsive Base Template](https://github.com/getpelican/pelican/issues/1704)


## Day 32: November 17, 2019, Sunday

### Today's Progress
Planned to write my first blog article out of the notes I have about setting my @getpelican blog up.
But, I got caught up on adding the "Attila" theme to it 😅

Now I have two post idea to write out 😬

 #100DaysOfWeb @TalkPython @PyBites

### Thoughts
First thing should be to write out how the blog is set up in general.
Though I would just extend the first article, but it turned out to be long enough for a separate article.

Also, should continue with making the default template responsive.
This does not need to be too crazy, just so that it looks fine on a small display.

### Link(s) to work
1. [Day 31 Commit -- Adding Blog Theme](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/032a357722ca3bfe8a70d60a6d306a8496579f67)
2. [Attila Theme for Pelican](https://github.com/arulrajnet/attila)


## Day 33: November 18, 2019, Sunday

### Today's Progress
Watched video lessons on @SQLAlchemy #100DaysOfWeb @TalkPython @PyBites
The definition of relationships and of the base class seem a little complex 😒 Hope i'll get it soon.

### Thoughts
Gonna try to get some coding done tomorrow.
Only watching videos does not feel good 😬

Need to get a grasp on the one-to-many relationship.
Why the hell do I need `parent_id` and `parent` on the child?
Shouldn't I get the id of the parent of the child with something like `child.parent.id`...

Gave up on the responsive pelican default theme, because [somebody else is already creating one](https://github.com/getpelican/pelican/issues/1704#issuecomment-554825227).


## Day 34: November 19, 2019, Tuesday

### Today's Progress
Played around with @SQLAlchemy relationships.
I see a lot more clear than yesterday 🤩
 #100DaysOfWeb @TalkPython @PyBites

### Thoughts
This lesson was not very good.
Not because of SQLAlchemy, but because that example app was way too complex (unnecessarily).
The structure of the app made it really hard to follow along.

Also in the lesson videos, the whole jumping around between the different views and features in PyCharm is not very helpful and way to fast.

Hope I can build something over the next two days to get some more hands on experience with SQLAlchemy.

### Link(s) to work
1. [Day 34 Commit -- SQL Alchemy Relationship Practice](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/777791a6f1c61bfc565e612a648aa436b425df68)


## Day 35: November 20, 2019, Wednesday

### Today's Progress
Started building an inventory and production line management system to practice @SQLAlchemy.
 #100DaysOfWeb @TalkPython @PyBites

### Thoughts
Practice definitely helps.

Still having a bit of a hard time understanding how to organize the session maker.
Apparently you only want one instance of the session maker.
That session maker instance is then supposed to be called every time I need a session.
Seems like it should be an application for a singleton.
Maybe have to look into that a bit more tomorrow.

### Link(s) to work
1. [Day 35 Commit -- SQL Alchemy Production Line Management](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/d3d3918793e2df4c203aa1c6bc9454eb81fe4bb6)
2. [Singleton in Python -- StackOverflow Thread](https://stackoverflow.com/questions/6760685/creating-a-singleton-in-python)


## Day 36: November 21, 2019, Thursday

### Today's Progress
Continued creating an inventory management system to practice @SQLAlchemy.
Created CLI to create, update and query data.
Spent a bit to much time on it though.

 #100DaysOfWeb @TalkPython @PyBites

### Thoughts
Unfortunately, I had not enough time today to build the whole system I wanted.
Too much time went into creating the UI.
Should be a good project to continue practising the relationships though.

### Link(s) to work
1. [Day 36 Commit -- SQL Alchemy Inventory Management](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/793dcb1d5ab6029568704c09a565197b7fe5c665)


## Day 37: November 22, 2019, Friday

### Today's Progress
Got first bit of intro to #pyramid @pylonsproject #100DaysOfWeb @TalkPython @PyBites
Really looking forward to learn more.
Been waiting for this 😊

Also set up first bit of lesson bill tracker app.

### Thoughts
Hope the next day explains more about the workings of the Pyramid framework.
So far it has been mainly the app setup.
Have not really worked with much of the Pyramid functionality.

### Link(s) to work
1. [Day 37 Commit -- Setup Pyramid Project](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/365d86dd4e514c1a2774cc3119d7586f201f5f02)


## Day 38: November 23, 2019, Saturday

### Today's Progress
Finished lesson videos on #pyramid intro #100DaysOfWeb @TalkPython @PyBites
Recreated the Bill Tracker demo app and added extended it with some authentication @pylonsproject

Really enjoying #pyramid framework.

### Thoughts
Still not feeling super excited about how the lesson was going.
The apps of choice seem too large sometimes and the automatic imports and so on in PyCharm (in the videos) do not help understanding the basic concepts.
Seems more designed to teach you PyCharm then the actual topic (Pyramid in this case).

### Link(s) to work
1. [Day 38 Commit -- Pyramid Exmaple Project](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/1dcda4ad1bddfc15b64b96bff44c12cbafed6c75)
2. [Pyramid Authentication](https://docs.pylonsproject.org/projects/pyramid/en/1.10-branch/tutorials/wiki2/authentication.html)


## Day 39: November 24, 2019, Sunday

### Today's Progress
Started creating a finance ledger app with #pyramid @SQLAlchemy from scratch #100DaysOfWeb @TalkPython @PyBites

So far only created the database models.
The navigating the starter and database modelling took quite some time.

Tomorrow I need to add the authentication, create the routes, views and the template for user interaction.

### Thoughts
The cookiecutter starter also included Alembic, which I haven't used before.
Three new topics at once is maybe a bit much at once.
Maybe I should have just started with a copy of the example project...


### Link(s) to work
1. [Day 39 Commit -- Ledger Project](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/4d6514b074302d058c68e2b78e7eb14c2f63cc5c)


## Day 40: November 25, 2019, Monday

### Today's Progress
😖 Kinda wastes the day with trying to figure out how to access the active pyramid config out side of a request.
Only to find that the preconfigured way to access it is much more elegant... hope to catch up with app dev tomorrow. #100DaysOfWeb @TalkPython @PyBites

### Thoughts
Working on a plane without internet does not really work, when you don't know yet what you are doing.

But, I need to pay attention to this habit.
Trying to force something fore hours and getting lost in these mental loops.
I could have just gone with the way it was set up and tried to find another way once I had the ability to actually look up stuff I do not know yet.

### Link(s) to work
1. [Day 40 Commit -- Ledger Project](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/b78bc81ca61490cbbccb9c9a9bed9423b6deee8a)


## Day 41: November 26, 2019, Tuesday

### Today's Progress
Learned about #react and build an app with it to show Python tips from @pybites website
 #100DaysOfWeb @TalkPython

Also went back to my ledger app and finally added some logic.

### Thoughts
React seems pretty straight forward.
Using JSX in the editor still needs some getting used to, because of the mix of HMTL and JavaScript syntax.
Not always sure how to set up the autocomplete options.

### Link(s) to work
1. [Day 41 Commit -- React](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/7ef7e9c0e2fec8a8c6a64794ca0e1d16fed80279)
1. [Day 41 Commit -- Ledger App](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/32bab4c2e100fc7b179a88efbca45e0ad4d28fec)


## Day 42: November 27, 2019, Wednesday

### Today's Progress
Built a #react todo app, that is pre-populated with data from an API.
 #100DaysOfWeb @TalkPython @pybites

Could not figure out how to add elements to the beginning of the array.
That only led to a repeated last element.
This must have something todo with the rendering engine.

### Thoughts
React seems quite nice.
Weird that I already managed to run in some sore of bug...

### Link(s) to work
1. [Day 42 Commit -- React Todo List](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/9fab7978723944123b7d183c2ac04f078728089d)



## Off-Day: November 28, 2019, Thursday

First thanksgiving in the US.


## Day 43: November 29, 2019, Friday

### Today's Progress
Yesterday, skipday for thanksgiving.
Learned some more about #React and recreated the example "Free Monkey" hangman variant #100DaysOfWeb @TalkPython @pybites

### Thoughts
React seems pretty straight forward.

### Link(s) to work
1. [Day 43 Commit -- React Hangman Game "Free Monkey"](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/2d65122102559d7fdfa4eacf9006a127ac1a0849)



## Day 44: November 30, 2019, Saturday

### Today's Progress
Do not know why, but it just came to be how I can implement a singleton in Python.
Just had to try it out :)

Created tic-tac-toe game with React.js  #100DaysOfWeb @TalkPython @pybites
Game logic works, but I can not reset the game 😖

### Thoughts
Guess the story with the singleton is an example of the brain working with out the conciousness knowing 🤔

Not sure what is wrong with the tic-tac-toe game...

### Link(s) to work
1. [Python Singleton](https://twitter.com/tbrlpld/status/1200894629953986561/photo/1)
2. [Day 44 Commit -- ](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/768b6b4d4a2198dbff209e7627c5d56f684ad83c)



## Day 45: December 1, 2019, Sunday

### Today's Progress
Read some of the #reactjs tutorial and fixed my tic-tac-toe game #100DaysOfWeb @TalkPython @pybites
Not sure what I really did wrong yesterday, but the game is much cleaner now.
State is only handled in the state and not represented in the rendering.

The reset button works now.

### Thoughts


### Link(s) to work
1. [Day 45 Commit -- React Tic Tac Toe ](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/12cc7d756fadbeed3d7c9a198e2eeefc50509c2e)


## Day 46: December 2, 2019, Monday

### Today's Progress
Watched intro videos to Django on #100DaysOfWeb @TalkPython @pybites yesterday.
Replayed the video steps to create a basic Django app layout today.

### Thoughts
I really do not like that Django does not validate anything when saving the models 🤨

### Link(s) to work
1. [Day 46 Commit -- Django Quotes App](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/5b833bb81e5c25e93278ee915ee430fae9bfa5c5)


## Day 47: December 3, 2019, Tuesday

### Today's Progress
Finished Django intro videos on #100DaysOfWeb @TalkPython @pybites
Recreated the demo Quotes CRUD app with function based views.

Tomorrow: turning the views into class based views.


### Link(s) to work
1. [Day 47 Commit -- Django Quotes App](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/cafea254157d5009b10ef0972a0722d6690c1d5b)


## Day 48: December 4, 2019, Wednesday

### Today's Progress
Finished Django intro by adding class based views with the same functionality as the function based views #100DaysOfWeb @TalkPython @pybites

So far, using the class based views is really simple when their base functionality is exactly what you need.

Also tried to continue with the tags feature for CAE Job Diary...

### Thoughts
This `django-autocomplete-light` that I wanted to use for the tags widget is kind of annoying me by now.
It makes it really hard to customize.
I can not catch the change events that the underlying `select2.js` is triggering.
And, well, let's not forget that it obviously does not validate the model you are saving...

Maybe I should look for alternate solutions or just build this my self.
Should not be that hard...
I could use the same approach, and directly use the `select2.js` for the rendering.


### Link(s) to work
1. [Day 48 Commit -- Django Quotes App](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/7d717acbcf3faad4dbe7d5cdd1b24ae8c367dca3)


## Day 49: December 5, 2019, Thursday

### Today's Progress
Learned about website testing with #Selenium #100DaysOfWeb @TalkPython @pybites

Reproduced the steps in the videos to create testing for an [existing website](https://pbreadinglist.herokuapp.com/).

### Thoughts
Trippy to see the browser just acting on its own 😊

### Link(s) to work
1. [Day 49 Commit -- Selenium](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/7d717acbcf3faad4dbe7d5cdd1b24ae8c367dca3)


## Day 50: December 6, 2019, Friday

### Today's Progress
Learned about #responder framework by @kennethreitz on #100DaysOfWeb @TalkPython @pybites
Recreated the simple demo API app! Very intuitive 👏

Also, triggered by a tweet by @kennethreitz, checked that the average float that is generated by Pythons random generator is in fact 0.5 😊

### Thoughts
Woohoo, half-time.

### Link(s) to work
1. [Day 50 Commit -- Responder](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/c6c47726d9f4f09a3ee288d7b0d3cd77b5748672)
2. [Kenneth Rietz's Tweet](https://twitter.com/kennethreitz/status/1202979569667641344)



## Day 51: December 7, 2019, Saturday

### Today's Progress
Learned how to use the Twilio SMS service #100DaysOfWeb @TalkPython @pybites

Tried to use it to create a simple two-factor authentication login with SQLAlchemy and the Responder framework.

### Thoughts
This was probably a bit much for one day.
Still need to make the database persistent (right now it is only in memory) and create a way to log out.
Also, the different pages should have a simple way of figuring out is the user is already logged in.


### Link(s) to work
1. [Day 51 Commit -- Twilio](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/804565dac95bf655352799a5c6a9bf84645ff0d6)


## Day 52: December 8, 2019, Sunday

### Today's Progress
Learned how to create full web apps with only Drag and Drop and Python on the #Anvil platform #100DaysOfWeb @TalkPython @pybites

Super easy. Recreated the example app.

### Thoughts
That is really easy.
Can definitely get you up and running pretty quick.


### Link(s) to work
1. [Day 52 Commit](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/04144cfe4ec8b335dd098306936cdf64590b718a)
2. [Anvil App](https://stunning-subdued-ask.anvil.app)


## Day 53: December 9, 2019, Monday

### Today's Progress
Learned about Django-Registration module #100DaysOfWeb @TalkPython @pybites

Tried to re-create the demo app. Registration form just reloads. No users created. 😟
What's going on here?


### Link(s) to work
1. [Day 53 Commit -- Django Registration](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/118edb94e3e6f30b3ba2d25b5ee82e24d9ca9222)


## Day 54: December 10, 2019, Tuesday

### Today's Progress
Spend basically all day debugging my Django registration #100DaysOfWeb @TalkPython @pybites

First the template was not showing the password criteria.
In trying to figure that out I created more issues that kept me debugging the rest of the day...

### Thoughts
This really highlights, why it is important to make sure the functionality works before the styling is applied.
In this case, using the custom template that introduces the styling did hide away the functionality of showing the field errors properly.
This cause my first issue with not being able to register accounts...

During that process I created the other issue... which of course is my fault.

### Link(s) to work
1. [Day 54 Commit -- Django Registration Debug](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/ac96f23a6a4425bebd9f5876db5ad7f2a5f5b05c)


## Day 55: December 11, 2019, Wednesday

### Today's Progress
Now that the the registration is working, finally finished adding the authentication to the Quotes app #100DaysOfWeb @TalkPython @pybites

Worked on setting up my dev environment to be able to contribute to `flake8-eradicate`.
I found a small bug in that tool and was asked by the maintainer to implement the fix he pointed out to me.
Still work in progress.
Using `peotry` in combination with `pyenv` seems to cause small issues.
Continuing tomorrow.


### Thoughts
🤔

### Link(s) to work
1. [Day 54 Commit -- Django Registration](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/571d64183219edb96d36f6ccc60b54734189d4b6)
2. [`flake8-eradicate` Bug Report](https://github.com/sobolevn/flake8-eradicate/issues/103)


## Day 56: December 12, 2019, Thursday

### Today's Progress
Got the development setup for `flake8-eradicate` up and running using `poetry` dependency manager

Couldn't figure out how to solve the bug I reported. Still working on that.

### Thoughts
🤔

### Link(s) to work
1. [`flake8-eradicate` Bug Report](https://github.com/sobolevn/flake8-eradicate/issues/103)


## Day 57: December 13, 2019, Friday

### Today's Progress
Travel day today. Only watched some videos on flask-login #100DayOfWeb @TalkPython @pybites

Gonna implement the demo app tomorrow.

### Thoughts
I know I said I wouldn't count the time spent on the videos in the course, but I will count today, because I really had no chance to catch up and I want to avoid getting my days and the course days completely out of sync.

### Link(s) to work
1. [#100DaysOfWeb in Python](https://training.talkpython.fm/courses/explore_100days_web/100-days-of-web-in-python)


## Day 58: December 14, 2019, Saturday

### Today's Progress
Recreated simple demo app with flask-login #100DayOfWeb @TalkPython @pybites

Extended the basic functionality a bit for nicer "user experience".

Password hashing and styling are still open.

### Link(s) to work
1. [Day 58 Commit -- Flask Login](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/d37199d2b1bf6e5d11e1027a5448e11a7bdb130e)


## Day 59: December 15, 2019, Sunday

### Today's Progress
Added password hashing to the flask-login app with `passlib`  #100DayOfWeb @TalkPython @pybites

Super easy 👏

### Link(s) to work
1. [Day 59 Commit -- Flask Login with Password Hashing](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/d37bcb78614420fe4f8e12b2899c4aa56dab610b)


## Day 60: December 16, 2019, Monday

### Today's Progress
Just created my first pull request (with actual code, not only documentation) to an open source project.
I solved a bug I found in the `flake8-eradicate` plugin, which tells you if your code contains commented out code.

Pretty exciting.
Waiting for the maintainer @sobolenv to respond 😊

### Link(s) to work
1. [`flake8-eradicate` -- Pull Request](https://github.com/sobolevn/flake8-eradicate/pull/106)


## Day 61: December 17, 2019, Tuesday

### Today's Progress
My first pull request to an open source project (`flake8-eradicate`) was accepted and merged today 🎉

Also, learned about `alembic` for `sqlalchemy` database migrations #100DaysOfWeb @TalkPython @PyBites
Setup and created some simple migrations in two apps to get the gist.
Very nice tool.
Looking forward to using this in other proper projects.

### Link(s) to work
1. [`flake8-eradicate` -- Pull Request](https://github.com/sobolevn/flake8-eradicate/pull/106)
2. [Day 61 Commit -- Using Alebic Migrations](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/cc31bccff8fc744ae7189eb6bc992fed7bdf83de)


## Day 62: December 18, 2019, Wednesday

### Today's Progress
No coding today.
Worked on shaping my new project and figured out the part that I want to work on the next two days.

After reading #shapeup by @rjs I trying to apply as much of it as makes sense for a personal project.

Looking forward to start implementing.


## Day 63: December 19, 2019, Thursday

### Today's Progress
Started working on "Heath", my new ledger app 😁
So far only the creation view exists.

It took me bit to figure out how to properly do test driven development with Pyramid and SQLAlchemy.

### Link(s) to work
1. [Day 63 Commit -- Ledger App](https://github.com/tbrlpld/Heath/commit/c70c67bdd6ed241113753e9e96436eb1f1b75a10)


## Day 64: December 20, 2019, Friday

### Today's Progress
Continued working on my new ledger app.

Functional testing of the routes/views is still not working, but cost me basically all day...

Hope to find some time in the next days to finish the minimal feature set I had planned for the last two days.

### Link(s) to work
1. [Day 64 Commit -- Ledger App](https://github.com/tbrlpld/Heath/commit/c0c5c972e1088e3006da11e7b18922d310f2cc1f)


## Day 65: December 21, 2019, Saturday

### Today's Progress
Finished the simple transactions CRUD for my ledger app.

Also, learned about Heroku on #100DaysOfWeb @TalkPython @Pybites
and created and deployed a minimal "Hello World" Flask app.

### Thoughts
Pyramid is somehow really confusing.
It seems like there are way too many ways to configure the whole thing of how to work in the views.
When should you `raise` one of their HTTP exceptions, and when should you `return` it?
It seems to cause different behaviour.

Even worse, why is the testing so complicated to set up?
Using their `DummyRequest` makes perfectly working views fail, because the `DummyRequest` does not have all the methods of a normal request.

Also, I had to completely leave the functional testing, e.g. testing of the templates etc., because I can't figure out why I is not initializing the DB...

### Link(s) to work
1. [Day 65 Commit -- Ledger App](https://github.com/tbrlpld/Heath/commit/78e73f5a60633864430a5f9bb2db2e8a5e5206af)
2. [Day 65 Commit -- Heroku](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/7515baa58bbc13c905ff0be8a594275ef2b31033)
3. [Heroku Hello World App -- Live](https://tbrlpld-hello.herokuapp.com/)


## Day 66: December 22, 2019, Saturday

### Today's Progress
Not much Code again.
Definitely no own project.

Going through the Pyramid tutorial.
Hope to get some better understanding of it to help me with my project issues.

### Link(s)
1. [Pyramid Quick Tutorial](https://docs.pylonsproject.org/projects/pyramid/en/latest/quick_tutorial/index.html)


## Day 67: December 23, 2019, Monday

### Today's Progress
Not much time today, due to late Christmas shopping 😏
Same thing as every year...

Did go through a few more steps on the Pyramid tutorial though.
Hope to get in some more tomorrow.

### Thoughts
So far, I do not think what I am learning though the tutorial will solve my testing issue (where I can not get the in-memory SQLit database to initialize when using functional tests with WebTest).
But, this definitely deepens my understanding of Pyramid and the different ways it can be configured.

### Link(s)
1. [Pyramid Quick Tutorial](https://docs.pylonsproject.org/projects/pyramid/en/latest/quick_tutorial/index.html)


## Day 68: December 24, 2019, Tuesday

### Today's Progress
Continued working on the Pyramid Quick Tutorial.
Third day in a row, and several hours. Not sure how this is "quick".

But this definitely increases my understanding of Pyramid a lot.

Hope it will help me with my database testing issue in the end.

### Thoughts
Hm, I am still not done, but tomorrow is a new topic on #100DaysOfWeb.
Kinda want to finish this, though.

### Link(s)
1. [Pyramid Quick Tutorial](https://docs.pylonsproject.org/projects/pyramid/en/latest/quick_tutorial/index.html)


## Off-Day: December 25, 2019, Wednesday

### Today's Progress
Took the day off for Christmas.


## Day 69: December 26, 2019, Thursday

### Today's Progress
Continued working on the Pyramid Quick Tutorial.
Went through the SQLAchemy section and could resolve similar issues as I have in Heath.
Some how this does not translate directly to how it is setup in Heath, because of the cookiecutter template that was used (the official one supplied by the Pyramid project).
Maybe I need to tear down the cookiecutter stuff and go more granular as in the tutorial to figure out where the issue is.

Also, learned about the Django REST framework on #100DaysOfWeb @TalkPython @PybBites
Seems pretty simple and straight forward.

### Thoughts
It is kind of annoying, that the cookiecutter code does not set up the functional testing correct.
I think it would, because this is a selection made in the template...

### Link(s)
1. [Pyramid Quick Tutorial](https://docs.pylonsproject.org/projects/pyramid/en/latest/quick_tutorial/index.html)


## Day 70: December 27, 2019, Friday

### Today's Progress
Used Django REST framework to turn an existing Quotes aggregation app into an API #100DaysOfWeb @TalkPython @PybBites

Wohoo 🎉 Finally figured out how to initialize the SQLAlchemy database in Pyramid functional testing!
Attach the db engine to the app registry was the solution 😊

### Thoughts
This is super relieving that I finally figured that out!


### Link(s)
1. [Day 70 Commit -- Django REST](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/ecaba88f98aaf2b9173ef934b4b737155f13b5b0)
2. [Heath Commit -- Resolving the database initialization issue](https://github.com/tbrlpld/Heath/commit/dc117239cf39913295aa28efd979700de04e138b)


## Day 71: December 28, 2019, Saturday

### Today's Progress
Finished the last two sections Pyramid Quick Tutorial.
Authentication - who are you.
Authorization - what are you allowed to do.

Tomorrow, finally back to my ledger application, now that that testing issue is resolved.


### Link(s)
1. [Pyramid Quick Tutorial](https://docs.pylonsproject.org/projects/pyramid/en/latest/quick_tutorial/index.html)


## Day 72: December 29, 2019, Sunday

### Today's Progress
Updated Django REST api to hide user field in input and set automatically to currently logged in user #100DaysOfWeb @TalkPython @PyBites
All credit to @bbelderbos for pointing me to the solution.

Also, worked on creating some tests for my ledger app.
So glad this is finally working.

### Link(s)
1. [Day 72 Commit -- Django REST User Input Fix](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/8da50b1612755fb3219b868be897060120d27ff5)
2. [Heath -- Functional Tests](https://github.com/tbrlpld/Heath/compare/functional-transaction-tests)


## Day 73: December 30, 2019, Monday

### Today's Progress
Learned about web scraping with beautiful soup #100DaysOfWeb @TalkPython @PyBites
Recreated the simple demo script to print all @TalkPython course names.

Also, converted tests in my ledger app from xUnit to pytest.
Really enjoying that style a lot more.
Seems to make the code a lot more reusable.

### Link(s)
1. [Day 72 Commit -- Web Scraping with BeautifulSoup](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/b28e4d5b34db153c0b968c6a94069d23653c577c)
2. [Heath -- Functional Tests](https://github.com/tbrlpld/Heath/compare/functional-transaction-tests)


## Day 74: December 31, 2019, Tuesday, New Year's Eve

### Today's Progress
Started incorporating BeautifulSoup into my functional tests for the ledger app #100DaysOfWeb @TalkPython @PyBites

Still wondering what the best way is to handle HTTP exceptions in #Pyramid @trypyramid @pylonsproject

### Link(s)
1. [Heath -- Functional Tests](https://github.com/tbrlpld/Heath/compare/functional-transaction-tests)


## Day 75: January 1, 2020, Wednesday, New Year's Day

### Today's Progress
Learned about the Newspaper package for scraping news articles #100DaysOfWeb @TalkPython @PyBites
Played with the REPL a bit. Not much today really...

### Thoughts
Not quite sure what to use this for.
Seems to be designed really only for one use case, and right now I do not have that one.
I think I rather focus on the general web scraping with BeautifulSoup.

### Link(s)
1. [Newspaper Package](https://newspaper.readthedocs.io/en/latest/)


## Day 76: January 2, 2020, Thursday

### Today's Progress
Continued adding more functional tests to my ledger app.
Parsing the responses with BeautifulSoup makes the data extraction a lot easier and more concise.
Glad I learned about this package #100DaysOfWeb @TalkPython @PyBites


### Link(s)
1. [Heath -- Functional Tests](https://github.com/tbrlpld/Heath/compare/functional-transaction-tests)


## Day 77: January 3, 2020, Friday

### Today's Progress
Learned how to create automated tweets with Tweepy #100DaysOfWeb @TalkPython @PyBites
Gonna try to automate my tweets from my log tomorrow.

Also, continued adding more tests to my ledger app.

### Link(s)
1. [Heath -- Functional Tests](https://github.com/tbrlpld/Heath/compare/functional-transaction-tests)


## Day 78: January 4, 2020, Saturday

### Today's Progress
Created script to automatically create tweets based on my daily log #100DaysOfWeb @TalkPython @PyBites

If everything worked out fine, this log entry is the first that should be tweeted automatically.

### Link(s)
1. [Day 78 Commit -- Logtweet Script](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/a35d71735b9bb6aa848532305e9c98c6600da3d2)


## Day 79: January 5, 2020, Sunday

### Today's Progress
Learned about Slack API and how to create a slash-command #100DaysOfWeb @TalkPython @PyBites

Also, tried to make logtweet script installable.
Don't know how to handle the config file yet.

### Thoughts
You can define additional files to be packaged with when using setuptools.
But, where do the additional files end up?
Can I access them? Can the user look there?

Also, does it even make sense to expect the config file near the module?
The config should probably be somewhere that is easy for the user to access.


### Link(s)
1. [Day 79 Commit -- Logtweet Script](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/c9305f4915eba4abd3f7f8cb61cc1281704150a5)


## Day 80: January 6, 2020, Monday

### Today's Progress
Just published "logtweet" on PyPi 🎉
Everybody who has their #100DaysOfCode log formatted like I can install and use it 😊
Install with `pipx install logtweet`.

 #100DaysOfWeb @TalkPython @PyBites

### Thoughts
Exciting. Although I don't think anybody but me will use it 😬

### Link(s)
1. [LogTweet on PyPi](https://pypi.org/project/logtweet/)
2. [LogTweet on GitHub](https://github.com/tbrlpld/logtweet)


## Day 81: January 7, 2020, Tuesday

### Today's Progress
Watched some videos on unit and functional testing web applications #100DaysOfWeb @TalkPython @PyBites

Didn't have time to code myself today, but will continue testing my ledger app tomorrow.

### Link(s)
1. [#100DaysOfWeb in Python](https://training.talkpython.fm/courses/explore_100days_web/100-days-of-web-in-python)


## Day 82: January 8, 2020, Wednesday

### Today's Progress
Restructured and extended the testing (especially functional) of my ledger app #100DaysOfWeb @TalkPython @PyBites

With these tests in place, I can now go into refactoring more confidently.

Looking forward to that.

### Thoughts
Just saw that three people have starred my `logtweet` script on GitHub 😄 Pretty exciting.

### Link(s)
1. [Day 82 Commit -- Testing Heath](https://github.com/tbrlpld/Heath/commit/5529a790debc0c14c208ae72f76fb2cabb3b40cf)
2. [Logtweet Stars on GitHub](https://github.com/tbrlpld/logtweet/stargazers)


## Day 83: January 9, 2020, Thursday

### Today's Progress
Pew, that was a lot today #100DaysOfWeb @TalkPython @PyBites.

Restructured my tests to be  easier to read.
Then, refactored my view functions into a class.
Definitely helps with keeping it DRY!


### Link(s)
1. [Day 83 Commit -- Refactoring Transaction Views in Heath](https://github.com/tbrlpld/Heath/commit/0bfa4030815336e677e1a15037a2816f6e5548cd)


## Day 84: January 10, 2020, Friday

### Today's Progress
Mainly shaping and refactoring of my ledger app 🤓📖💸

Started implementing a feature so separate transaction by account.
Used #TDD through out. #100DaysOfWeb @TalkPython @PyBites.

### Link(s)
1. [Day 84 Commit -- Staring Accounts in Heath](https://github.com/tbrlpld/Heath/compare/0bfa40308153...305931195efc)


## Day 85: January 11, 2020, Saturday

### Today's Progress
Learned about AWS Lambda #100DaysOfWeb @TalkPython @PyBites.

Followed along the lesson example and built a little #Flask app that checks Python code against #PEP8 through a lambda function.

I guess the code check it in a Lambda isolates against possibly malicious code.

Also read a bunch about "serverless" technology in general.
It seems pretty interesting not having to setup the server myself, but only worry about the app.
Because, the Lambda functions are not limited to simple function like I used.
You could potentially host an entire web apps logic on it. The database might need to be somewhere else, but the app could run as a function.

For Python, [Zappa](https://github.com/Miserlou/Zappa) seems to make that process pretty simple.


### Link(s)
1. [Day 85 Commit -- PEP8 Lambda](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/689e1e4134d4e4df1fbac2c955a97fd09384ae61)


## Day 86: January 12, 2020, Sunday

### Today's Progress
Started working on a link shortener app hosted on AWS Lambda with Zappa and DynamoDB #100DaysOfWeb @TalkPython @PyBites.

Setting up a custom domain for the gateway API ate a lot of time.

This is also the first time for me working with AWS DynamoDB.
So I needed to look into that too.

### Thoughts
All the hosted DB options seem kind of expensive.
Why is that so? Seems like you can get compute time pretty easy, but if you want to store a few rows, it's gonna cost you.

Is that because of the disk space involved? And the need to backup the databases and keep the data consistent over multiple locations?

Well, that kind of kills the attractiveness of "serverless" options.
It seems cheaper to just get a machine with root access and then run the DB and app your self.

[Vultr](https://www.vultr.com/products/cloud-compute/) seems pretty neat for that. You can get a machine with root access from $2.50 per month. And that is the capping price. If you use less, you are charged less...


### Link(s)
1. [Day 86 Commit -- Link Shortener Lambda](https://github.com/tbrlpld/100daysofweb-with-python-course/compare/689e1e4134d4e4df1fbac2c955a97fd09384ae61..60cf279fbc555ab5f8731b97a1d269d01bad407a?diff=unified)


## Day 87: January 13, 2020, Monday

### Today's Progress
Not much today.
Continued with the link AWS URL shortener #100DaysOfWeb @TalkPython @PyBites
Turned the DB layer into a class.


### Link(s)
1. [Day 87 Commit -- Link Shortener Lambda](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/9643dae840e6c7b45aea597519564323ca293e03)


## Day 88: January 14, 2020, Tuesday

### Today's Progress
Finished my URL shortener [s.lpld.io](https://s.lpld.io) 😄 #100DaysOfWeb @TalkPython @PyBites
Flask app deploy with Zappa to AWS Lambda and backed by DynamoDB.

Updated logtweet to use my URL shortener by default 😬

Bit.ly service can still be configured if desired.

### Link(s)
1. [Day 87 Commit -- Link Shortener Lambda](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/806eec4af04c9a9ca4f8fe1f4b7f9e0f8d4945a3
)
2. [Logtweet Release 0.1.2](https://pypi.org/project/logtweet/0.1.2/)


## Day 89: January 15, 2020, Wednesday

### Today's Progress
Learned about deploying web apps on Linux #100DaysOfWeb @TalkPython @PyBites

Not much code today, but I fixed my URL shortener to deal with trailing newlines in the long URLs.

The trailing newline caused the first link I published on twitter to fail... How embarrassing 😓

Also, read a bunch about CDN and how to get a database server up and running.
Think this would be a great addition to the course. So far all courses and tutorials I have gone through only use SQLite.
But setting up a separate database server that can be reached online seems like a crucial skill for a web developer to me. I think I want to  do that over the next few days.

### Link(s)
1. [Day 89 Commit -- Link Shortener Lambda Fix](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/b3ff50f7a6c9a591a0fe2544be80e4af30b9a3a0)


## Day 90: January 16, 2020, Thursday

### Today's Progress
No code today. Only worked on getting my server configured #100DaysOfWeb @TalkPython @PyBites

Definitely need to remember to install the rsa keys before disabling password login 😅


## Day 91: January 17, 2020, Friday

### Today's Progress
Again, not much code, but I finished setting up an NGINX server and host a Pyramid app with uWSGI #100DaysOfWeb @TalkPython @PyBites

Really like the pattern to have the server config files (e.g. the NGINX site config) in the repo.

Same goes for the service definition that makes sure the app is automatically started with the sever. Once the repo is on the server, you just link to the config/definition file.

Maybe combining this with git hooks and pushing directly to the webserver could be an awesome addition.

I already deleted the Droplet where I was hosting the exmaple app.
Tomorrow I want to start setting up the database server.
This is going to be the first time I will have a production ready database available. :) The next thing I will need is an app that makes use of it ^^


## Day 92: January 18, 2020, Saturday

### Today's Progress
No "code". Wrote up my notes for an initial server setup as a possible blog post.

Also, started setting up a database server for future applications ^^ #100DaysOfWeb @TalkPython @PyBites


## Day 93: January 19, 2020, Sunday

### Today's Progress
Learned about Vue.js and recreated today's part of the demo application #100DaysOfWeb @TalkPython @PyBites

### Link(s)
1. [Day 93 Commit -- Movie Data Frontend](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/474bf452e15d2661bbe7eda8d6b5e8066fcd6a22)


## Day 94: January 20, 2020, Monday

### Today's Progress
Finished the Vue.js section and implemented the movie app backed by an API #100DaysOfWeb @TalkPython @PyBites

### Link(s)
1. [Day 94 Commit -- Movie Data Frontend](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/f50bd688381aafda3f3b0f65f140a9e4a25b216a)


## Day 95: January 21, 2020, Tuesday

### Today's Progress
Again, not much code.
Been messing with my server setup.
Trying to establish an ssh tunnel between app and db server #100DaysOfWeb @TalkPython @PyBites


## Day 96: January 22, 2020, Wednesday

### Today's Progress
And once again, not much code but more server setup @PyBites

App and db server are now communicating though an ssh tunnel that is established as a service. The linked article helped a lot.

### Link(s)
1. [Everything CLI -- SSH Tunneling for Fun and Profit](https://www.everythingcli.org/ssh-tunnelling-for-fun-and-profit-autossh/)



