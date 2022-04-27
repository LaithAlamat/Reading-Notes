# Identity and Authentication

ASP.NET Core Identity:

- Is an API that supports user interface (UI) login functionality.
- Manages users, passwords, profile data, roles, claims, tokens, email confirmation, and more.

Users can create an account with the login information stored in Identity or they can use an external login provider. Supported external login providers include Facebook, Google, Microsoft Account, and Twitter.

Identity is typically configured using a SQL Server database to store user names, passwords, and profile data. Alternatively, another persistent store can be used, for example, Azure Table Storage.

## Microsoft identity platform

- An evolution of the Azure Active Directory (Azure AD) developer platform.
- Unrelated to ASP.NET Core Identity.

## Identity Components

All the Identity-dependent NuGet packages are included in the ASP.NET Core shared framework.

The primary package for Identity is Microsoft.AspNetCore.Identity. This package contains the core set of interfaces for ASP.NET Core Identity, and is included by Microsoft.AspNetCore.Identity.EntityFrameworkCore.

## Claims

A Claim represents a single fact about the user. It could be the user's first name, last name, age, employer, birth date, or anything else that is true about the user. A single claim will contain only a single piece of information.

Claims are represented by the Claim class in ASP.Net Core. It's most common constructor accepts two strings: type and value

- Authenticate
  Gets the user’s information if any exists (e.g. decoding the user’s cookie, if one exists)
- Challenge
  Requests authentication by the user (e.g. showing a login page)
- SignIn
  Persists the user’s information somewhere (e.g. writes a cookies)
- SignOut
  Removes the user’s persisted information (e.g. deletes the cookies)
- Forbid
  Denies access to a resource for unauthenticated users or authenticated but unauthorized users (e.g. displaying a “not authorized” page)

  ## Authentication Handlers

  Authentication handlers are components that actually implement the behavior of the 5 verbs above.

A middleware is a module that can be inserted into the startup sequence and is run on every request.

## Authentication and Authorization Flow
All of these components must be used together in the auth system in order to successfully authenticate and authorize a user to access a resource. The process begins with the unauthenticated user sending a request for a resource that requires authorization to access.

- The request arrives at the server.
- The authentication middleware calls the default handler's Authenticate method and populates the HttpContext.User object with any available information.
- The request arrives at the controller action.
- If the action is not decorated with the [Authorize] attribute, display the page and stop here.
- If the action is decorated with [Authorize], the auth filter checks if the user was authenticated.
- If the user was not, the auth filter calls Challenge, redirecting to the appropriate signin authority.
- Once the signin authority directs the user back to the app, the auth filter checks if the user is authorized to view the page.
- If the user is authorized, it displays the page, otherwise it calls Forbid, which displays a 'not authorized' page.
