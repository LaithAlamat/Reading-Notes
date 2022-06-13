# ***View Components***

- View components are similar to partial views, but they're much more powerful. View components don't use model binding, they depend on the data passed when calling the view component.

- A view component consists of two parts:

    1. The class, typically derived from ViewComponent
    2. The result it returns, typically a view.

- Like controllers, view components must be public, non-nested, and non-abstract classes. 

- Supports constructor dependency injection



## ***View Components Uses***

- Renders a chunk rather than a whole response.
- Includes the same separation-of-concerns and testability benefits found between a controller and view.
- Can have parameters and business logic.
- Is typically invoked from a layout page.