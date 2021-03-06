# Technical FAQ

This FAQ is organised into the following sections. Some problems fit more than
one section, so ensure you've properly checked if you don't think your question
is answered (search the text of the page using the "find" option, which is under
the "edit" menu on most browsers).

1. [How to Ask
   Questions](#1-how-to-ask-questions-or-how-to-find-your-own-answers) 
2. [Problems Running Code](#2-problems-running-code) 
3. [Problems with Git](#3-problems-with-git) 
4. [Getting the Most Out of Codio](#4-getting-the-most-out-of-codio)

If your issue doesn't seem to appear on the page, check "[How to Ask
Questions](#questions)" first, before asking a question. If you think an issue
needs to be added to this FAQ, [contact me](mailto:p.mcminn@sheffield.ac.uk).

<a id="questions"></a>
### What this FAQ covers

This FAQ covers technical issues only. **If you're experiencing a team issue, or
have a question about the team project**, check out the check the [Assignment
FAQ](https://vle.shef.ac.uk/webapps/blackboard/execute/content/blankPage?cmd=view&content_id=_5820338_1&course_id=_96428_1&mode=reset)
on Blackboard. If this does not answer your question, you should contact your
supervisor, or wait until your next meeting with them.

## 1. How to Ask Questions (Or, How to Find Your Own Answers) 

I don't believe that there are stupid questions, but there are definitely *lazy*
ones. It's not that lazy questions are annoying – that's not the issue here –
it's that you're actually denying yourself a learning opportunity by not putting
in the effort to find the answer yourself. This is not just about honing your
skills in quickly finding the information you need, but also how to resolve
problems and debug issues with code yourself. 

Before asking a question, try to find the answer yourself. Finding your own
answers is an important skill that will be invaluable in the rest of your
degree, and also your future career. So start to develop it now! 

### Finding Your Own Answers: Some Tips 

1. **Check the lecture slides**. Seems obvious. But you'd be surprised how many
   questions we get that are answered by a lecture slide that covered what you
   wanted to know. There may be a slide or an example that you missed that
   already explains something you wanted to know about or demonstrates some code
   similar to what you want to do. Look there first. 

2. **Check this FAQ**. To save time reading through the entire FAQ, use the
   "Find" feature in your browser to search for certain words appearing on the
   page to do with your query (e.g. "Git", "Capybara", etc.)

3. **Check the discussion forums on Blackboard** to see if your question has
    already been answered. If it hasn't, don't post your own question just yet.
    There are more steps to try first.

4. **Check the docs**. Your question may be answered by the documentation for
   [Sinatra](http://sinatrarb.com/documentation.html),
   [SQLite](https://www.sqlite.org/docs.html) (see also [SQLite's SQL
   docs](https://www.sqlite.org/lang.html)),
   [Sequel](https://sequel.jeremyevans.net/documentation.html) (see also
   [Sequel's GitHub page](https://github.com/jeremyevans/sequel), which has lots
   of handy examples), [RSpec](https://relishapp.com/rspec), and
   [Capybara](https://rubydoc.info/github/teamcapybara/capybara/master) (see
   also the handy [cheat sheet](https://devhints.io/capybara)).

5. **Use Google**. If you're unsure how to go about googling technical issues,
   or want to be more effective at using Google to find answers to programming
   questions, watch this video – "[Art of Googling as a
   Programmer](https://www.youtube.com/watch?v=JIV7wuihew8)" – for some tips.
   It's a bit Python-centric, but the principles apply to any programming
   language on any platform – and pretty much anything technical.

**If all of the above fails, you can ask a question.** See the next section on
how to go about doing this.

### How Do I Go About Asking Questions?

To ensure you get a timely answer that resolves your problem, ensure you follow
these steps:

* **For specific technical questions about your team project**, ask your
  demonstrator. You can ask in the lab, or via Slack if the issue arises between
  labs and cannot wait until the next one. Bear in mind that your demonstrators
  are students too. They have assignments and deadlines of their own, so they
  may not respond immediately.

* **If your demonstrator cannot help you**, post a question in the appropriate
  forum in the [Discussion
  Board](https://vle.shef.ac.uk/webapps/discussionboard/do/conference?toggle_mode=read&action=list_forums&course_id=_96428_1&nav=discussion_board_entry&mode=view)
  on Blackboard. 
  
  However, *don't post large chunks of your project's code in the forum*. If
  your problem only involves one or two lines of code that aren't important,
  that is fine; or, you might be able to obfuscate the code to demonstrate the
  same problem, but without using code directly lifted from your project.
  
  If your problem involves large segments or involves the whole project, then
  leave your team number and ensure you've pushed everything to the main branch
  of your repository (along with a detailed explanation of the problem you're
  experiencing). We can then clone your code and try to replicate the issue
  ourselves. 

* **Please don't email staff about technical issues directly.** Although staff
  email addresses are listed on Blackboard, they're only there as a *last
  resort*. It is highly unlikely that you won't get a response using one of the
  methods above.

Naturally, when asking a question, help us to help you by including as much
relevant information as possible. Screen shots are fine, but don't just post
these without any context. If you don't provide all the information needed, we
won't be able to resolve the issue.

## 2. Problems Running Code 

### When I try to run `sinatra` I get a `sinatra: command not found` message at the terminal, and my code refuses to run.

Have you cloned this repository on Codio? If you did, you haven't run the
`install` script yet to set up your Codio box. See the instructions in the
[README.md file in the `code` directory of this repository](code/) as to how to
do this. It's also covered in the video on the [Getting
Started](https://vle.shef.ac.uk/webapps/blackboard/execute/content/blankPage?cmd=view&content_id=_5796998_1&course_id=_96428_1&mode=reset)
page on Blackboard.

Note that you have to clone the COM1001 and run the `install` script for every
Codio project/box that you intend to work with. It's the `install` script that
installs the `sinatra` script, so you won't be able to do any development unless
you've completed this step. (You can't, for instance, have a separate Codio
project/box for the COM1001 repository, and another for developing your team
project.)

### When I try to run one of the examples from the lectures in the `code` directory of this repository, it crashes with an error.

This is because you need to install the gems for the example first. In the
terminal, ensure you have changed directory to the one containing the example,
and type the following:

```
bundle install
```

The gems installed are the ones listed in the `Gemfile` in that directory. (Open
the file to view what gems these are.)

You may need to refresh your memory on gems and Gemfiles. If so, go back to the
material from the Autumn Semester (in particular, see Unit 7: Ruby Gems). You
can also try Google of course for more information.

### When I run my web application or an example, Codio display a "401 Authorization Required" message instead of the proper web page.

This is because Codio doesn't think you're logged into Codio on the web browser
you're trying to use. Open a tab and check you are indeed logged in. If this
doesn't work, try clearing out your cookies, log into Codio and try again. 

If the issue persists, it's likely an issue with your browser, so try a
different one. If this still doesn't work, then it might be a machine setting,
so contact me (or try Codio support). The university's machines should always
work, so this facility should always be available to you, even if you cannot run
examples with Codio from your own machine. 

### When I run my web application or an example, Codio display a "502 Bad Gateway" error instead of the proper web page.

This is likely because you're not using the `sinatra` command to run your code
and using the `ruby` command instead. Make sure you're using the `sinatra`
command!

### When I try to do a `gem install`, Codio tells me I do not have "write permissions".

That's because you should be using `bundler` instead. If you're trying to run
one of the code examples from the lectures, see the answer to the [question on
Bundler
above](#when-i-try-to-run-one-of-the-examples-from-the-lectures-in-the-code-directory-of-this-repository-it-crashes-with-an-error).
If it's for your own project, you should write a `Gemfile` and use that to run
`bundler` instead. See the code examples in this repository for how to do that.  

### I can't see the changes I made to my Sinatra application.

You have to stop (go to the terminal window and press "control" and "c") and
then restart the web server (triggered by the `sinatra` command you used to
start your application) each time you change any Ruby code in it (an exception
is `.erb` files, changes for which can be seen without stopping and restarting).

This is a tedious thing to have to keep doing during development! So I recommend
using `sinatra/reloader`, as I showed you in the [Sinatra
Basics](slides/1-3-sinatra-basics.pdf) lecture (see the last slide). Using
`sinatra/reloader` means that Sinatra will listen out for changes to your Ruby
files and reload them when you make changes, meaning that you do not have to
keep stopping and restarting the web server each time you make a change to your
project.

Note that you don't need to restart the web server if you only made changes to
view files. 

### I can't see the changes I made to my CSS / my CSS is not updating. 

Ensure that your browser is not caching your CSS files (i.e., using a stored,
out of date copy, rather than a fresh version from your web application).

Clear out your browser cache, or switch off caching altogether. Google how to do
this for the browser you're using.

### Our team project works for my teammates but crashes with an error on my Codio box.

These kinds of issues ("it works for my teammates but not for me") are almost
always (99% of the time) to do with differences in the gems that are installed
on different Codio boxes. If you think about it logically, what else could be
the difference in setup between your Codio box and theirs, since each box is
practically identical in terms of its configuration at the beginning. When
trying to debug, try to think about differences between "when it works" and
"when it doesn't". 

If you issue a `gem list` command at the terminal, you will be able to see a
list of gems installed on your box, and you can compare it with that of your
teammates'. (The list can be quite long!)

You can also use the `reset_gems` command to reset the gems installed on your
box.

Make sure that your project has all the gems it needs by keeping your `Gemfile`
up to date. This is the key to avoiding these kinds of problems in the first
place. 

### I'm getting an error message `cannot load such file -- sequel (LoadError)`. I have the sequel gem installed, so I'm confused as to what is going on.

You need the `sqlite3` gem installed as well. Make sure both the `sequel` and
the `sqlite3` gems are part of your project's `Gemfile`.

### What are the gems we will need for the team project?

Depending on how far through the lectures we are, we may not have encountered
all of these, so don't worry about the ones you don't recognise (yet):

* **Core gems** include `sinatra`, `puma` (the web server), `require_all` (for
  automatically "requiring" all Ruby files in a directory), `rubocop` (for
  coding standards and style checking). 

* For the **database**, you'll need at least `sequel` and `sqlite3`. Don't
  forget the `sqlite3` gem, otherwise you'll get some confusing error messages.  

* For **encrypting user data** (i.e., to preserve data confidentiality), you'll
  need `openssl`.

* For **code style checking**, you'll need `rubocop`. To extend style checking
  to RSpec and Sequel code, you'll also need `rubocop-rspec` and
  `rubocop-sequel` respectively.

* For **testing**, you'll need at least `capybara` (for end-to-end tests),
  `rack-test`, `rspec`, and `simplecov` (for coverage tracking).

Note that some of these gems may already be installed on a fresh Codio box. It's
good practice to include them in your Gemfile regardless for
development/deployment environments where they aren't.

### When testing, my application seems to behave differently with Capybara compared to when it's being used for real. 

This is often to do with differences between the "test" database and the
"production" database. If certain data is not present in the test database, the
application may behave differently. If you're experiencing some differing
behaviour, the first thing you can check is the log files produced by Sequel.
Check the queries are the same when the application is being run in "production"
mode compared to when it is being tested.


## 3. Problems with Git

### I cannot clone my team's repository.

You keep getting asked for your password, but you're getting error messages.
This is because GitLab uses SSH keys to authenticate you rather than passwords.
If you're being asked for your password, it's probably because you did not set
up GitLab with your Codio SSH keys last semester. That is, you didn't complete
both parts of Unit 8, which is about Git. I'd strongly recommend you go back and
do both of these units, because Git is very important this semester.

To set up your SSH keys, sign into Codio, then click your username in the bottom
left profile. Under "My Account", there should be a menu item called "SSH Keys".
If you click this link, you'll be taken to a page with a grey box at the top,
with your public SSH key in it. Ensure that you select and copy the entire
contents of this box (and *only* the contents of the box). Now, log into Gitlab
(https://git.shefcompsci.org). Click the icon in the top right of the page to
reveal a drop-down box, and select "Preferences". Select "SSH Keys" from the
sidebar that appears. In the big text box that appears, paste your SSH key. In
the title box, enter "Codio". Then click the "Add key" button.

Other possible reasons:

* You're trying to clone another team's repository. Check your team number!

* There's been an administrative error, and you don't have the necessary
  permissions to clone your team's repository. This is the most unlikeliest of
  the possibilities, so check you have done all of the above first. However, it
  does happen from time to time, so if you're still experiencing problems, this
  is one of the few occasions where you can [send me – Phil McMinn – an
  email](mailto:p.mcminn@sheffield.ac.uk). Make sure that you include your
  Sheffield computer account username in the body of the email.

## 4. Getting the Most Out of Codio

### I don't really like Codio. Can I use my own machine to develop on instead?

We'd prefer you didn't. Codio makes it really easy for us to provide a
standardised environment to students in which we can help with common problems.
Fixing individual machine setups is very time consuming and our priority is
helping with programming questions and issues. 

It's not *impossible* to develop everything on your own machine. However, this
means you installing Ruby and getting everything working yourself — we are
unable to provide support for students' individual machines. While getting Ruby
set up tends to be relatively easy on Linux on Mac machines, Windows users
typically encounter more problems. Also, do not forget your team members on your
project who may prefer to use Codio, opening up various possibilities for
incompatibilities and problems. Finally, remember that the team project will be
marked using Codio. So everything needs to work on Codio, because the markers
will not be debugging your code to get it to run.

There are ways to use Codio in a way that is friendlier to more experienced
programmers, however – see the answer to the next question. 

### I've heard it's possible to use VSCode on Codio. Is that true?

Yes! Visual Studio Code [(VSCode)](https://code.visualstudio.com) is a popular
text editor and IDE for many languages, and may be used in a web browser on
Codio itself. Assuming you have followed in the instructions in the first
lecture and have everything setup in Codio, then you will have a Codio box
already up and running. In Codio, go to "Tools", then "Install Software". Scroll
down the list and select "VSCode". VSCode will be now available at a special URL
in your web browser for use with your Codio files. The URL you need to access it
depends on your Codio box name. Your Codio box name is the subdomain of your
Codio Box domain, which Codio tells you in the preamble of every Terminal
session that you start. For example, my Terminal session prints out the
following:

```
 *
 * Welcome to the Codio Terminal!
 *
 * https://docs.codio.com/project/ide/boxes/#overview
 *
 * Your Codio Box domain is: everton-fan.codio.io
 *
```

This means my box name is ``everton-fan``. This means my URL for VSCode, if I
installed it, would be https://everton-fan-4000.codio.io. Note that this URL is
essentially the same as the Base URL of your web applications launched from
Codio (as discussed in lectures), but using port 4000.

### Is it possible to SSH into Codio, and therefore use my own machine to develop?

Yes, but it's potentially tricky to setup.  SSHing into your Codio box from your
text editor/IDE on your own machine gives you the best of both worlds — the use
of your preferred development environment, but with the ease of Ruby already
being set up for you on Codio, and you using the same platform as everyone else.
However, you will need to navigate the instructions for doing this yourself —
again, we are unable to provide assistance. See
https://docs.codio.com/common/develop/ide/boxes/access.html. Instructions for
your text editor/IDE vary of course, depending on what you're using — here are
some useful pointers for VSCode, as an example:
https://code.visualstudio.com/docs/remote/ssh.
