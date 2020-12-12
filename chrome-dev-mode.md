### Google Chrome Lunch

For testing purpusose we want to switch on or off some chrome functionalities.

For example, to test an API, we may want to disable CORS protection in browser.

This in particular and many other features of Crome browser can be disabled or

enabled by runing special instance of the browser.

<br>

First of all, we need to create a directory for temporary chrome user:

```
mkdir test
```

This directory is required to lunch Chrome using any other settings then default,

as well as to store temorary files and settings (like cookies e.t.c) during this

session.

<br>

Next, we are ready to start chrome in detached mode with sequrity disabled:

```
nohup google-chrome \
    --user-data-dir=~/test \
    --disable-web-security \
    --new-window about:blank & disown
```

<br><br>

### Axios and ajax requests

In order to make ajax calls from front-end testing environment many different

approaches can be used. The most simple I have found is to use [axios](https://github.com/axios/axios).

It can be installed to the current web page by running following command in console:

```
const e = document.createElement('script');
e.src = "https://unpkg.com/axios/dist/axios.min.js";
document.head.appendChild(e);
```

After that axios instance would be available with `axios` variable.
