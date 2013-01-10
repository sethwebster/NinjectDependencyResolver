# Ninject Dependency Resolver for Web Api
---
A work based on Brad Wilson's gist -- not sure if it's his original work or not -- for supplying a Dependency Resolver that works with WebApi and Ninject.

#### To install:

##### Nuget

1. First, install via Package Manager Console


  		Install-Package Ninject.WebApi.DependencyResolver
  	
		
2. Then, open up your Ninject Bootstrapper file, usually in ~/App_Start/Ninject*.cs, and add this line (in CreateKernel for example):

		System.Web.Http.GlobalConfiguration.Configuration.DependencyResolver = new Ninject.WebApi.DependencyResolver.NinjectDependencyResolver(kernel);    
       
3. Register and perform your bindings as normal

