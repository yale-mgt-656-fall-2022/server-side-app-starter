## Sever side applications

This is a minimal example of an HTTP server (equivalently, a web server, or a server side app.)
Go is a great language in which to write HTTP servers. E.g. see
fans [here](https://blog.iron.io/how-we-went-from-30-servers-to-2-go/)
and [here](https://www.youtube.com/watch?v=bAQ9ShmXYLY)
and [here](https://talks.golang.org/2016/applicative.slide#1)
and [here](https://medium.com/@kevalpatel2106/why-should-you-learn-go-f607681fad65).
There are many more...that's just what jumped out at my searching
around in a few minutes.

One of the nicest aspects of writing servers in Go is that everything
you need is included in [Go's standard library](https://golang.org/pkg/).
That is, it's "batteries included"&mdash;you don't have to learn another
framework in order to be productive.

### How to complete this assignment

Completing this assignment is easy. You need to edit `main.go` to make
it respond to HTTP GET requests at `/nickname` with your class nickname.
E.g. my nickname is "bald-chicken" and so my webserver should respond
at `/nickname` with "bald-chicken". It also needs to respond at the `/`
URL, but the content isn't important.


### Fly.io instructions

Once your app is working, you should deploy it to
[Heroku](https://heroku.com), [fly.io](https://fly.io), or some other
place if you're a ninja and prefer to host it elsewhere. 
Honestly, [fly.io's online instructions](https://fly.io/docs/languages-and-frameworks/golang/)
are fine. I can't improve upon them here. Deploying to fly.io took a few minutes
for me. Like, really long! Afterward type `flyctl open` to get your app's URL.

### Heroku instructions

To deploy to Heroku,
you'll need to sign up for an account. Then you'll need
to create a Heroku app. From my computer I would do that with a command
like this, assuming I am in the directory where this file resides
and you're on the main branch of your repo.

```
heroku login
heroku create
git push heroku main
```

You might want to type "git status" before all that. If you have uncommitted
changes, clearly they won't be pushed to Heroku 😜. Also Heroku costs money
now!

You can find out the URL of your app running on Heroku by using the `heroku`
command as follows: `heroku apps:info`. This should display something like

```
=== example-app-69977
Auto Cert Mgmt: false
Dynos:
Git URL:        https://git.heroku.com/example-app-69977.git
Owner:          your@emailaddress.com
Region:         us
Repo Size:      0 B
Slug Size:      0 B
Stack:          heroku-18
Web URL:        https://example-app-69977.herokuapp.com/
```

In the above example, the URL that includes `herokuapp` is the one I want
you to submit. This is where your app is running online.

### Testing (grading) your app

You can test your app at
[https://grading.656.mba](https://grading.656.mba).

You can see my completed homework running
at [http://server-side-app.solutions.656.mba/](http://server-side-app.solutions.656.mba/)

## Tips

- Make sure you commit your work using git and push it to GitHub
- Deploy your app to Heroku/fly.io
- Submit both your GitHub repo URL and your app (Heroku or fly.io) URL via
  the class website. If you don't do so, or you do so inaccurately,
  I won't be able to give you a grade that reflects your true
  awesomeness.
