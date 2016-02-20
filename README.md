#Angular Review - 20 Feb 2016

### What should be in a Controller vs. Service?


### How to persist data inside a controller when it is refreshed?
- When a page is refreshed, or the browser is closed and reopened, all js files are reinstantiated, and all variable are "reset".
- Options to save data include localstorage or database.
- In SPA (single page application), when you "route" to a new view, the page is not refreshed. However, the controllers are reinstantiated each time you route to the new view, whereas, the services (or "singletons") are not. So, you can set save data in services that you don't want to lose by routing to a new view. This is kind of like localstorage, except it will not persist through a browser closing or refreshing.

### $http vs. $q
#### When do you use $q over $http


### High Level Overview
#### JSON, RESTful, AJAX


