ASP.NET Core
============

Recently discovering some things about ASP.NET Core 
(see [github](https://github.com/sylvanmist/expert-pancake-aspnetcoreapp))

It claims to provide the following:

* Unified story for building web UI and web APIs
* Cloud-ready configuration system
* Dependency injection
* Host on IIS, Nginx, Apache, Docker
* Cross-platform
* FOSS

ASP.NET Core supports the following features:

* MVC pattern
* Razor pages (page-based programming model)
* Razor markup
* Tag helpers (server-side code)
* Multiple data formats and content negotiation
* Model binding
* Model validation

I was successful in getting a basic app up and running on
Fedora 27.

Seamlessly integrates with Angular, React, and Bootstrap (have 
not tested this as yet, but soon).

Steps
=====

Run `dotnet new razor -o project_name` from the command line.
