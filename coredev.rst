.. _coredev:

How to Become a Core Developer
==============================

What it Takes
-------------

When you have consistently contributed patches which have met quality standards
to be committed without requiring extensive rewrites, you may qualify for
commit privileges and become a core developer of Python. You must also work
well with other core developers (and people in general) as you become an
ambassador for the Python project.

Typically a core developer will offer you the chance to gain commit privilege.
The person making the offer will become your mentor and watch your commits for
a while to make sure you understand the development process. If other core
developers agree that you should gain commit privileges you are then extended
an official offer.

You may request commit privileges yourself, but do not be surprised if your
request is turned down. Do not take this personally! It simply means that other
core developers think you need more time contributing patches before you are
able to commit them without supervision.

XXX list of people


Gaining Commit Privileges
-------------------------

When you have been extended an official offer to become a Python core
developer, there are several things you must do.

Mailing Lists
'''''''''''''

You are expected to subscribe to python-committers, python-dev,
python-checkins, and one of new-bugs-announce or python-bugs-list. See
:ref:`communication` for links to these mailing lists.


Issue Tracker
'''''''''''''

If you did not gain the Developer role in the `issue tracker`_ before gaining
commit privileges, please say so. This will allow issues to be assigned to you.

It is expected that on the issue tracker you have a username in the form of
"first_name.last_name". If your initial issue tracker username is not of this
form, please change it. This is so that it is easier to assign issues to the
right person.


SSH
'''

You need to generate an SSH 2 RSA key to be able to commit code. You may have
multiple keys if you wish (e.g., for work and home). Send your key as an
attachment in an email to python-committers (do not paste it in the email as
SSH keys have specific formatting requirements).

Your SSH key will be set to a username in the form of "first_name.last_name".
This should match your username on the issue tracker.

You can verify your commit access by looking at
http://www.python.org/dev/committers which lists all core developers by
username. You can also execute the follow command and look for the word
"success" in the output::

    ssh pythondev@svn.python.org

For Windows users using Pageant::

    c:\path\to\putty\plink.exe pythondev@svn.python.org

An entry in the ``Misc/developers.txt`` file should also be entered for you.
Typically the person who sponsored your application to become a core developer
makes sure an entry is created for you.


Sign a Contributor Agreement
''''''''''''''''''''''''''''

Submitting a `contributor form for Python`_ licenses any code you contribute to
the Python Software Foundation. While you retain the copyright, giving the PSF
the ability to license your code means it can be put under the PSF license so
it can be legally distributed with Python.

This is a very important step! Hopefully you have already submitted a
contributor agreement if you have been submitting patches. But if you have not
done this yet, it is best to do this ASAP, probably before you even do your
first commit so as to not forget.


.. _contributor form for Python: http://www.python.org/psf/contrib/



Read/Write Checkout
'''''''''''''''''''

With your commit privileges working and your contributor form submitted, you
can now get a read/write checkout of the code. URLs for read/write checkouts
are different than those for read-only checkouts as SSH is used instead of
HTTP.

For the development branch, you can check out the development branch with::

    svn co svn+ssh://pythondev@svn.python.org/python/branches/py3k

Make the appropriate changes to the URL to checkout maintenance branches by
removing ``py3k`` and replacing it with the name of the branch you want.


Responsibilities
----------------

As a core developer, there are certain things that are expected of you.

First and foremost, be a good person. This might sound melodramatic, but you
are now a member of the Python project and thus represent the project and your
fellow core developers whenever you discuss Python with anyone. We have a
reputation for being a very nice group of people and we would like to keep it
that way.

Second, please be prompt in responding to questions. We are all volunteers so
what little free time one can dedicate to Python should be spent being
productive. If you have been asked to respond to an issue or answer a question
and you put it off it ends up stalling other people's work. It is completely
acceptable to say you are too busy, but you need to say that instead of
stringing people along. This obviously applies to anything you do on the issue
tracker as well.

Third, please list what areas you want to be considered an expert in the
``Misc/maintainers.rst`` file (including stdlib modules). This allows triagers
to direct issues your way when they involve an area you are an expert in. But,
as stated in the second point above, if you do not have the time to answer
questions promptly then please remove yourself as needed from the file so that
you will not be bothered in the future. Once again, we all understand how life
gets in the way, so no one will be insulted if you remove yourself from the
list.

And finally, enjoy yourself! Contributing to open source software should be fun
(overall). If you find yourself no longer enjoying the work then either take a
break or figure out what you need to do to make it enjoyable again.