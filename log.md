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
Recreated Google landing page from 1998. 

### Thoughts
Client side form input validation is pretty helpful, because it is immediate.
Doesn't replace server side validation, but is helpful in it's responsiveness. 

### Link(s) to work

1. [#100DayOfWebInPython -- HTML & HTML 5](https://github.com/tbrlpld/100daysofweb-with-python-course/tree/master/days/005-008-html5)
2. [Day 6 Commit](https://github.com/tbrlpld/100daysofweb-with-python-course/commit/52fec0b1b494fdc778887c0945ac4e9b550d7079)



