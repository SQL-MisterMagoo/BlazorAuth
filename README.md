### Sample Require Auth By Default

This repo is configured for "Authorized by default" - meaning every "Page" in the pages folder will require Authorization.

It demonstrates how to allow anonymous access (the Index and Authentication pages) where required.

#### Steps to do this in your Blazor Webassembly application (starting from an application that already has the default Blazor Auth setup)

1. Add an `_Imports.razor` file to the `Pages` folder
`@attribute [Authorize]`
*Note: this makes all _pages_ in this folder require an Authenticated user.

2. Add the `AllowAnonymous` attribute to the Authentication and Index razor files
`@attribute [AllowAnonymous]`

#### Further

Add `@attribute [AllowAnonymous]` anywhere that a user is not required.
Add more refined `Authorize` attributes anywhere that requires more control.
