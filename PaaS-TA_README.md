## HTTP Basic Authentication Enabled
> $ vi src/code.cloudfoundry.org/gorouter/common/http/basic_auth.go
```diff
func (x *BasicAuth) ServeHTTP(w http.ResponseWriter, req *http.Request) {
        y := extractCredentials(req)
        // Beware of the hack
        if authenticatedEndpoint(req.URL.Path) && (y == nil || !x.Authenticator(y[0], y[1])) {
-               w.Header().Set("WWW-Authenticate", "Basic")
-               w.WriteHeader(http.StatusUnauthorized)
-               w.Write([]byte(fmt.Sprintf("%d Unauthorized\n", http.StatusUnauthorized)))
+               w.Header().Set("WWW-Authenticate", "None")
+               w.WriteHeader(http.StatusBadRequest)
+               w.Write([]byte(fmt.Sprintf("%d StatusBadRequest\n", http.StatusBadRequest)))
        } else {
                x.Handler.ServeHTTP(w, req)
        }
```
