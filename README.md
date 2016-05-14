Injecter
========

This is a dependency injector specifically designed for use with Yours Bitcoin.
In order to allow injecting dependencies, Yours Bitcoin classes provide an
"inject" method that makes a new class with injected dependencies.  However,
that method by itself presents a problem, because it creates a new class every
time it is used, leaving the burden of caching the classes to the user. Thus
the injector allows us to easily wrap an inject method that keeps a cache of
the created classes, lowing memory burden, and allowing the instanceof operator
to work correctly.
