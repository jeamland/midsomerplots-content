# MidsomerPlots content
This is a Midsomer Murders plot generator, available as a Node.js package and as an open web API, as used in the [@midsomerplots](https://twitter.com/midsomerplots) Twitter bot ([code](https://github.com/matthewberryman/midsomerplots)) and [Alexa skill](https://www.amazon.com/Across-the-Cloud-Pty-Ltd/dp/B07K87CPPQ) ([code](https://github.com/matthewberryman/midsomerplots-Alexa))

# Use as a Node.js module:

```javascript
const midsomerplots = require('midsomerplots-content');

// need to pass a seed = an integer, here just the time
midsomerplots.generate(Math.round((new Date()).getTime()/1000));
```

# Web API

```shell
curl "https://midsomerplots.acrossthecloud.net/plot?seed=n"
```
for some integer n (if ommitted, will default to current Unix time in seconds)

Example esponse:
```json
{
    "plot": "An underappreciated archivist is found quilted to death. Suspicion falls on Midsomer Magna’s New Age commune, angry that massive union mobilisation might threaten to force the local diamond mine to close."
}
```


