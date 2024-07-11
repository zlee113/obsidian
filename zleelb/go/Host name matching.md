Helpful to redirect HTTP requests to URL

```
mux := http.NewServeMux() 
mux.HandleFunc("foo.example.org/", fooHandler) 
mux.HandleFunc("bar.example.org/", barHandler)
mux.HandleFunc("/baz", bazHandler)
```