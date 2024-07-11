Backend focused learning book for GO Lang

- Chap 1 intros creating a [[GO module]], the canonical name or the identifier for a project

- Chap 2.1 Goes on to do a simple hello world program in the newly created module. 

- Chap 2.2 we start to get into web application basics, comprised of three different parts:
	- [[Handler]] following the [MVC pattern](https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93controller)
	- A router, [[servemux]] in go
	- A web server, which in go can be established and listen for requests as a part of the application itself
	- We also get some additional information into [[go run command]]

- Chap 2.3 Routing requests 
	- adding additional handler functions to add to handler
	- Trailing slashes in route patterns
		- URL path has to match exactly
		- having a subtree path with a trailing slash allows it to be a wildcard ending like "/\*\*"
		- That is why having a single slash is a catch all, it means anything after can be a path
	- Restricting subtree paths
		- Opposite of just having a trailing slash using "/{$}" to require the path to match just the one slash
	- Additional info
		- URL paths are automatically sanitized so if you use . or .. it will automatically redirect
		- If a subtree path is registered you will automatically be redirected so if you go to /foo and /foo/ is registered you will be redirected automatically.
		- [[Host name matching]], you can include host names in route patterns 
		- [[Default servemux]] using http 
- Char 2.4 Wild card route patterns 
	- Can use { } in route to have a specific wildcard segment filled into its place
	-  