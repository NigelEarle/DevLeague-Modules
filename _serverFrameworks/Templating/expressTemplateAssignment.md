## The Challenge
The CEO just called and she forgot to develop a new product for the big tradeshow event this year! She needs to present something to appease the hungry shareholders in exactly one hour. Thinking quickly, you realize that a new templating engine would be super cool. It's needs to be done quickly, so it doesn't need to be pretty, but it should have basic functionality. Your challenge is to develop a templating engine for Express from scratch for her to present in under an hour to save the company, impress the shareholders, and achieve enternal glory!

### How it will work:
Add functionality to your Express app so that it will be able to render .dlr files (short for DevLeague Rules). When you make a request to the home page, index.dlr will be rendered as HTML.

### The requirements:
- Use the extenstion .dlr
- The tempalting engine will replace anything surrounded with double bling '$$'
  - (i.e. $$title$$)
- You will pass in your dynamic data through your routes
- You have one hour
- It doesn't need to be perfect  - it just needs to work well enough to make it look like it working


#### Hint:
To develop template engines for Express, use the [app.engine(ext, callback)](http://expressjs.com/en/4x/api.html#app.engine) method to create your own template engine.
