AlphaMail: An Email Analysis Tool

Created by Sandip Nirmel and Dhruv Mohnot of Harvard University

Last Modified: December 3, 2017


Summary:

AlphaMail is an email analysis tool that allows users to learn some important metrics about their inboxes. With a simple, easy-to-use interface, users are only a couple of clicks away from a clean, one-page summary of their inbox. AlphaMail makes use of the Gmail API.

Getting Started:

To use AlphaMail, you will need to install several packages, if you do not already have them installed onto your local machine. Below, we provide the command-line prompts that you should use to install those packages. However, please do note that different machines require different versions of each command. We have delineated these different versions, to the best of our knowledge and based on our own experiences. If you find that the running the first version of the command results in an error, please try running the second version of the command. Additionally, please note that the order in which these installations are performed is very important.

sudo easy_install pip 

sudo chown -R $USER /Library/Python/2.7

pip install Jinja2

pip install Flask

pip install flask_session

pip install --upgrade oauth2client 	

NOTE: alternate version of above:  pip install --user --upgrade oauth2client

pip install --upgrade google-api-python-client 

NOTE: alternate version of above: pip install --user --upgrade google-api-python-client

pip install --upgrade google-auth google-auth-oauthlib google-auth-httplib2

NOTE: alternate version of above: pip install --user --upgrade google-auth google-auth-oauthlib google-auth-httplib2

pip install --upgrade requests

pip install backports.functools_lru_cache

pip install cycler

python -mpip install matplotlib

pip install mpld3


Additionally, please note that older machines might have an older version of the "six" library, with which our application is not compable. 

If you have an older machine, you may want to take the following steps to ensure compatibility with our application. We cannot guarantee that these steps will allow our application to run on your machine, since we were using newer versions of the Macintosh computer and hence did not run into these issues. We gleaned these steps from various StackOverflow threads discussing similar issues. 

First, in your command line, execute the following command:

sudo pip install -I google-api-python-client==1.3.2

Additionally, try adding the following line of code to your ~/.bashrc file:

export PYTHONPATH=/Library/Python/2.7/site-



Usage:

After completing the "Getting Started" steps listed above, you are ready to use the AlphaMail application.

First, download the zip file (titled "finalproject") containing the source code for our project. Unzip the file, and you will get a folder titled "finalproject." Move this folder to your computer's root directory (i.e. Macintosh HD), so that this folder resides alongside Applications, Users, and the like. Open up your command line, and navigate into your root directory (i.e. Macintosh HD). Next, navigate into the finalproject folder, using the following command: cd finalproject

Now, you are in the working directory for our project. Now, execute the following command in your command line: python application2.py 

After a few seconds, the following text should appear on your command line: "Running on http://localhost:8080/ (Press CTRL+C to quit)". Copy the http://localhost:8080/ and paste it into your Internet browser, and click enter. 

Next, you should be directed to a screen that is titled "AlphaMail" and has a single button that says "Log In". Click this button, and you will be redirected to the Google sign-in interface page, where you will be able to select which of your email accounts you would like to analyze using AlphaMail. If prompted by the Google interface, make sure to allow our application to access your email account. 

Now, you will need to wait 10-30 seconds, depending on the speed of your internet connection, so that our application can run. After that time, you will redirected to a page that displays graphics and statistics about your inbox. Enjoy!=
