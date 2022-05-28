# ***MVC*** 

MVC is a design pattern or architecture which helps in developing the web application in a most efficient way when compared with the traditional ASP.NET Web Application.

## ***MVC Vs API***

+ In traditional ASP.NET web application approach, the user action and view (UI) are combined, i.e., the web page, say, Sample.aspx and code behind Sample.aspx.cs which has the action logic are both tightly coupled, whereas in MVC, the View only deals with UI of the page and the user actions are defined in Controller.

+ In any web based application, a user initiates the requests which are nothing but actions. So, for action based requirement, ASP.NET Web Application follows the View based architecture which is not so efficient. MVC is action-based architecture. Based on the action, an appropriate View is displayed. The organization of the code inside MVC is very clean and organized.

+ In ASP.NET, View State is used to maintain the state of the web page. Maintaining the state means maintaining the data between post backs for a user. This makes the web page heavy which, in turn, makes the trips to server inefficient. In MVC, we don’t have View State to store the state information.

+ ASP.NET MVC can be used to develop light-weight applications. This design pattern will also be useful when an application is being developed by large team as it can be controlled and maintained effectively. And one more advantage is that a few developers can work on View (UI part) and others on Models and others on Controller logic. And later, all the three can be integrated. It can also be used for large-scale applications.

+ For RAD Models and small scale applications, it’s always better to go with traditional ASP.net Web Application Framework.

## ***MVC Layers***

+ **Model** layer represent the objects in our Application. Model is also a class which has all the objects and its properties and methods defined in it.

+ **View** Layer has all the html controls which define the UI of the application. Here in MVC, we don’t have drag and drop option for controls as we don’t use server controls. Instead we use Razor Engine available with Visual Studio by default which helps in rendering the View.



+ **Controller** basically handles the request from user. It is the heart of the MVC application as everyone say. It is responsible to handle the request and return a response to user by loading appropriate View with data from Model.

    Controller maps the incoming user requests to appropriate Controller actions with the help of process called Routing.

## ***Azure DevOps***

Azure DevOps provides developer services for allowing teams to plan work, collaborate on code development, and build and deploy applications. Azure DevOps supports a collaborative culture and set of processes that bring together developers, project managers, and contributors to develop software. It allows organizations to create and improve products at a faster pace than they can with traditional software development approaches.

You can work in the cloud using Azure DevOps Services or on-premises using Azure DevOps Server.

### ***Azure DevOps Services***
+ Azure Repos provides Git repositories or Team Foundation Version Control (TFVC) for source control of your code.
+ Azure Pipelines provides build and release services to support continuous integration and delivery of your applications.
+ Azure Boards delivers a suite of Agile tools to support planning and tracking work, code defects, and issues using Kanban and Scrum methods.
+ Azure Test Plans provides several tools to test your apps, including manual/exploratory testing and continuous testing.
+ Azure Artifacts allows teams to share packages such as Maven, npm, NuGet, and more from public and private sources and integrate package sharing into your pipelines.

## ***Tag Helpers***

Tag Helpers enable server-side code to participate in creating and rendering HTML elements in Razor files. 

There are many built-in Tag Helpers for common tasks - such as creating forms, links, loading assets and more - and even more available in public GitHub repositories and as NuGet packages. Tag Helpers are authored in C#, and they target HTML elements based on element name, attribute name, or parent tag.

Tag Helpers reduce the explicit transitions between HTML and C# in Razor views. In many cases, HTML Helpers provide an alternative approach to a specific Tag Helper, but it's important to recognize that Tag Helpers don't replace HTML Helpers and there's not a Tag Helper for each HTML Helper.

### ***What Tag Helpers Provide**

+ An HTML-friendly development experience

    For the most part, Razor markup using Tag Helpers looks like standard HTML. Front-end designers conversant with HTML/CSS/JavaScript can edit Razor without learning C# Razor syntax.

+ A rich IntelliSense environment for creating HTML and Razor markup

    This is in sharp contrast to HTML Helpers, the previous approach to server-side creation of markup in Razor views. Tag Helpers compared to HTML Helpers explains the differences in more detail. IntelliSense support for Tag Helpers explains the IntelliSense environment. Even developers experienced with Razor C# syntax are more productive using Tag Helpers than writing C# Razor markup.

+ A way to make you more productive and able to produce more robust, reliable, and maintainable code using information only available on the server


+ Most built-in Tag Helpers target standard HTML elements and provide server-side attributes for the element.

## ***Bootstrap***
Bootstrap is a giant collection of handy, reusable bits of code written in HTML, CSS, and JavaScript. It’s also a frontend development framework that enables developers and designers to quickly build fully responsive websites.

### **Bootstrap Advantages**


1. Its responsive grid


    Defining custom breakpoints for each column is a snap using their extra small, small, medium, large, and extra large breaks. You can also simply stick to the default as it might already meet the needs of your site.

2. Its responsive images

    Bootstrap comes with its own code for automatically resizing images based on the current screen size. 



    It can even change the shape of your images with the addition of classes, and that’s without going back and forth between the code and your design software.

3. Its components

    Bootstrap comes with a whole barrelful of components you can easily tack onto your web page, including:


4. Its JavaScript


    Bootstrap also allows developers to take advantage of over a dozen custom JQuery plugins. This library gives you even more room to play with interactivity, offering up easy solutions for modal popups, transitions, image carousels, anda plugin called scrollspy, which automatically updates your navigation bar as you scroll through a page.

5. Its documentation

    Bootstrap’s documentation is some of the best we’ve ever seen. Every piece of code is described and explained in explicit detail on their website.



6. Its customizability

    One of the main critiques when it comes to frameworks such as Bootstrap is their size—the weight they throw around can really slow down your application upon first load.




