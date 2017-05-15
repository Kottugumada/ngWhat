## No Provider for string.
You have created a child component and now are trying to pass values from the root module.

This is because Angular instantiates the child class by its own and tries to inject in it the parameters you define at its constructor level. 
That directly implies that there is no associated provider for it.

Also, if you want to reference children components from the parent, you could leverage the `@ViewChild` decorator to reference the child component from the parent by injection.
Here is a Plunkr demo: 
http://plnkr.co/edit/7EAMrF
