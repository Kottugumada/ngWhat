## Proxy Config and CORS
So, you have set up your api project and now are trying to access the api endpoint.
You may do this by updating your proxy.config.json
`{
  "/api": {
    "target": "http://mysiteapi:8080",
    "secure": false
  }
}`
That was your locally hosted api.
If you are trying to access it from a different origin. You might have to allow the origin.
the most common way of doing this would be using OWIN CORS.
I will deal with the details of doing this in a later chapter.
Assume, that you have that going.
Now you wish to host your api on the cloud and access it locally.
So that when you hit that api from http://localhost:4200 you should be able to proxy across borad.
To be able to do that you would have to add one more attribute `changeorigin`
So, now you proxy config would look something like this:
`{
  "/api": {
    "target": "http://mysiteapi.azurewebsites.net",
    "changeOrigin": true,
    "secure": false
  }
}`

