# ***MVC Forms***

In the Model-View-Controller (MVC) pattern, the view handles the app's data presentation and user interaction. A view is an HTML template with embedded Razor markup. Razor markup is code that interacts with HTML markup to produce a webpage that's sent to the client.

In ASP.NET Core MVC, views are .cshtml files

Use layouts to provide consistent webpage sections and reduce code repetition. Layouts often contain the header, navigation and menu elements, and the footer.

Partial views reduce code duplication by managing reusable parts of views.

View components are similar to partial views in that they allow you to reduce repetitive code, but they're appropriate for view content that requires code to run on the server in order to render the webpage. View components are useful when the rendered content requires database interaction.

Views that are specific to a controller are created in the Views/[ControllerName] folder. Views that are shared among controllers are placed in the Views/Shared folder.

Razor markup starts with the @ symbol. Run C# statements by placing C# code within Razor code blocks set off by curly braces ({ ... }).

You can display values within HTML by simply referencing the value with the @ symbol.

Views are typically returned from actions as a ViewResult, which is a type of ActionResult.

When an action returns a view, a process called view discovery takes place. This process determines which view file is used based on the view name.

A view file path can be provided instead of a view name. If using an absolute path starting at the app root (optionally starting with "/" or "~/"), the .cshtml extension must be specified:

    return View("Views/Home/About.cshtml");

You can also use a relative path to specify views in different directories without the .cshtml extension. Inside the HomeController, you can return the Index view of your Manage views with a relative path:

    return View("../Manage/Index");

ViewBag isn't available by default for use in Razor Pages PageModel classes.

Since ViewData and ViewBag refer to the same underlying ViewData collection, you can use both ViewData and ViewBag and mix and match between them when reading and writing values.

### ***ViewData Vs ViewBag***
- **ViewData**
Derives from ViewDataDictionary, so it has dictionary properties that can be useful, such as ContainsKey, Add, Remove, and Clear.
Keys in the dictionary are strings, so whitespace is allowed.
Any type other than a string must be cast in the view to use ViewData.
- **ViewBag**
Derives from Microsoft.AspNetCore.Mvc.ViewFeatures.Internal.DynamicViewData, so it allows the creation of dynamic properties using dot notation (@ViewBag.SomeKey = <value or object>), and no casting is required. The syntax of ViewBag makes it quicker to add to controllers and views.
Simpler to check for null values. 
<br></br>
Isolate CSS styles to individual pages, views, and components to reduce or avoid:

Dependencies on global styles that can be challenging to maintain.
Style conflicts in nested content.

<br><hr></br>

## ***Benefits of Using Views***

- The app is easier to maintain because it's better organized. Views are generally grouped by app feature. This makes it easier to find related views when working on a feature.
- The parts of the app are loosely coupled. You can build and update the app's views separately from the business logic and data access components. You can modify the views of the app without necessarily having to update other parts of the app.
- It's easier to test the user interface parts of the app because the views are separate units.
- Due to better organization, it's less likely that you'll accidentally repeat sections of the user interface.

<br><hr></br>

## ***Form In ASP.NET MVC***
Forms are very essential and basic thing that every programmer has to learn.
1. Forms - Weakly Typed (Synchronous)
2. Forms - Strongly Typed (Synchronous)
3. Forms - Strongly Typed AJAX (Asynchronous)
4. Forms – HTML, AJAX and JQUERY


### **Advantage and Disadvantage of Weakly Typed Form**

- Advantage:
1. It is easy to create a form using Weakly Typed mechanism
2. Mostly used when you need to create a form with one or two input items.

- Disadvantage:
1. Because, it is not strongly typed so IntelliSense doesn't help you.
2. Have higher chance of getting exception and runtime error messages.
3. Very difficult to manage when forms have multiple input items and controls.
4. It is very clumsy when you need to add or remove some input items.

### **Strongly Typed**
we send objects (model) instead of sending each item as parameter. It is easy to maintain because you don't need to remember each input item and IntelliSense will show you automatically the each item.

### **STRONGLY TYPED AJAX (ASYNCHRONOUS)**
Asynchronous AJAX form is a very magical way to submit data to the controller without happening page load. Asynchronous AJAX Forms simply post back the data to the controllers and update the only that part of the page, which has to display output.

To make this happen, we will use JQuery-Unobstrusive-AJAX

### **PURE HTML FORMS WITH AJAX AND JQUERY**
In this method, you can not only send data from input controls but can also use html elements like <p>…</p>, <span>…</span> to send data to controllers. This is pure JQuery and AJAX query.