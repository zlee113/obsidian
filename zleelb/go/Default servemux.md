Allow user to register routes without declaring a servemux

```
func main() { 
	http.HandleFunc("/", home) 
	http.HandleFunc("/snippet/view", snippetView) 
	http.HandleFunc("/snippet/create", snippetCreate) 
	
	log.Print("starting server on :4000") 
	
	err := http.ListenAndServe(":4000", nil) log.Fatal(err) 
}
```

LOOK INTO THIS MORE LATER

Behind the scenes, these functions register their routes with something called the default
servemux. This is just a regular servemux like we’ve already been using, but which is
initialized automatically by Go and stored in the http.DefaultServeMux global variable.
If you pass nil as the second argument to http.ListenAndServe(), the server will use
http.DefaultServeMux for routing.
Although this approach can make your code slightly shorter, I don’t recommend it for two
reasons:
- It’s less explicit and feels more ‘magic’ than declaring and using your own locally-scoped servemux.
- Because http.DefaultServeMux is a global variable in the standard library, it means any Go code in your project can access it and potentially register a route. If you have a large project codebase (especially one that is being worked on by many people), that can make it harder to ensure all route declarations for your application are easily discoverable in one central place. It also means that any third-party packagesthat your application imports can register routes with http.DefaultServeMux too. If one of those third-party packages is compromised, they could potentially use http.DefaultServeMux to expose a malicious handler to the web. It’s simple to avoid this risk by just not using http.DefaultServeMux.
So, for the sake of clarity, maintainability and security, it’s generally a good idea to avoid
http.DefaultServeMux and the corresponding helper functions. Use your own locallyscoped servemux instead, like we have been doing in this project so far