# ***Razor Pages***
 Razor Pages is subset of MVC on ASP.NET Core. support for Razor Pages comes with ASP.NET Core MVC meaning that Razor Pages application is technically MVC application. Also Razor Pages have same features as MVC views.

 ## ***Application Structure*** 
 - Application structure is similar to MVC but there are no folders for controllers and views. The folder called Pages contains all Razor views that in this context are called “pages”. These pages are like regular MVC views but they also contain code that for MVC is held in controller classes.

 - Program and Startup classes are exactly the same as for MVC applications. 

- Pages are always marked with @page directive that tells view engine this is Razor page and not a regular MVC view.

- when you make a request the default ASP.NET Routing configuration will attempt to locate a Razor Page for that request in the Pages folder.

- It simply looks for a page with the name used in the request (.cshtml) and routes directly to it.

- The Razor Page then acts as though it were a controller action.

- For a .cshtml file to qualify as a Razor Page, it must live in the Pages folder and include @page in its markup.

- Every Razor Page can have a corresponding Page Model.

- If we stick to the default conventions, ASP.NET will expect that model to have the same name as the corresponding Razor page but with a .cs appended.

- Your application code lives in these models, specifically in methods for the different HTTP verbs (e.g. GET, POST).

 ## ***Razor page with no code-behind***
Now let’s see how previous page looks without code-behind file. It works exactly like the version with code-behind class.

    @page
    @{
    ViewData["Title"] = "About";
    }
    @functions {
    public string Message { get; set; }
 
    public void OnGet()
    {
        Message = "Your application description page.";
    }
    }
    <h2>@ViewData["Title"].</h2>
    <h3>@Message</h3>
 
    <p>Use this area to provide additional information.</p>
Methods and properties are defined in @functions section. I just moved the contents of page model to page itself and it works. In practice it’s better idea to have those code-behind files and views clean from code as code in views is not so easy to test using automated tests. Also if views grow more complex over time it’s only good if growing codebase is in code files.

## ***Tutorial***

- To enable the RazorPages add this in the Program.cs

        builder.Services.AddRazorPages();
        app.MapRazorPages();

- Make sure to put the @page directive to the view  file

## ***CSS isolation***
Isolate CSS styles to individual pages, views, and components to reduce or avoid:

Dependencies on global styles that can be challenging to maintain.
Style conflicts in nested content.
To add a scoped CSS file for a page or view, place the CSS styles in a companion .cshtml.css file matching the name of the .cshtml file. In the following example, a Index.cshtml.css file supplies CSS styles that are only applied to the Index.cshtml page or view.

Pages/Index.cshtml.css (Razor Pages) or Views/Index.cshtml.css (MVC):

    h1 {
        color: red;
    }
## ***ViewData attribute***
Data can be passed to a page with ViewDataAttribute. Properties with the ViewData attribute have their values stored and loaded from the ViewDataDictionary.

In the following example, the AboutModel applies the ViewData attribute to the Title property:


    public class AboutModel : PageModel
    {
        [ViewData]
        public string Title { get; } = "About";

        public void OnGet()
        {
        }
    }


## ***Custom Routes***

Custom routes
Use the @page directive to:

- Specify a custom route to a page. For example, the route to the About page can be set to /Some/Other/Path with @page "/Some/Other/Path".

- Append segments to a page's default route. For example, an "item" segment can be added to a page's default route with @page "item".

- Append parameters to a page's default route. For example, an ID parameter, id, can be required for a page with @page "{id}".