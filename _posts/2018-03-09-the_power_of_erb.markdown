---
layout: post
title:      "The Power Of ERB"
date:       2018-03-09 20:49:41 +0000
permalink:  the_power_of_erb
---



Having now progressed my way through a majority of the Sinatra labs, I would have to say one of the most powerful tools I have learned thus far is ERB. First things first, ERB is a templating engine and stands for **E**mbedded **R**u**B**y, it's used as an extension for our view files within the MVC file structure. Sinatra and ERB work hand in hand throughout a simple web application, proven by the fact that Sinatra is preconfigured to look for ERB files in a directory called views. Views themselves represent how things look and are displayed in our application to the user.

The simplest way to show how to effectively use ERB within your code is demonstrated in the following example:

Let’s say we have a simple web application with a single page, represented by a file named index.erb within the views folder. With Sinatra, ERB files consist of HTML and Embedded Ruby, which is essentially just Ruby code written within HTML code. This index.erb file is what the user will actually see rendered within their browser. In order for this index.erb file to be rendered, a GET request will have to be called within the controller. Now since we are calling on the index or home page, as this site only has the one page the GET request will look like this:

```
get '/' do
	erb :index
end
```

The '/' is the route of our index or home page. In the second line we are calling on our index.erb file to be rendered. To put it quite literally in the above code snippet we are telling the controller to at this specific route render this specific ERB file. 

Now, lets say we decided to add a contact page to our simple web app. The path or route to this specific page will be /contact. The first thing we will need to do is create a new ERB file within the views folder, its always convenient to name our files something that will be easily understandable to other programmers, so we will go ahead and name this file contact.erb. This is where our HTML and Embedded Ruby that makes up the contact page will live. Our next step is to make our controller aware of this new route so that it is able to be rendered when our users go to this page of our web app. This is accomplished with the following code snippet:

```
get '/contact'do
	erb :contact
end
```

The '/contact' is the route or path of our contact page and as with the index page, in the second line we are calling on our file to be rendered. This is all quite literally the very basics of ERB and how it is used to make our simple web applications aware of files and give our controller the ability to renderer these files at a specific route. 

Every time I learn something new about programing, as I have said before, I feel as though its power is nearly limitless, though I know that to not be the case, as everything has its limits. It truly is great learning new things and to see how such a relatively simple piece of code has the ability to do such complex tasks. 
