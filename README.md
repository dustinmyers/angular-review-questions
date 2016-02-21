#Angular Review - 20 Feb 2016

### What should be in a Controller vs. Service?
- A controller works to build the $scope object up with the data that we want to display on the DOM. It isn't used to manipulate data, and doesn't do AJAX (http) requests.
- The services are the "heavy lifters". In our service, we get data from AJAX requests, manipulate and reform that data, or perform the necessary "business logic" and then make that data acessible to the controller.

### How to persist data inside a controller when it is refreshed?
- When a page is refreshed, or the browser is closed and reopened, all js files are reinstantiated, and all variable are "reset".
- Options to save data include localstorage or database.
- In SPA (single page application), when you "route" to a new view, the page is not refreshed. However, the controllers are reinstantiated each time you route to the new view, whereas, the services (or "singletons") are not. So, you can set save data in services that you don't want to lose by routing to a new view. This is kind of like localstorage, except it will not persist through a browser closing or refreshing.

### $http vs. $q
#### When do you use $q over $http
- Running a $http request DOES return a promise. However, in some cases, we need to give ourselves even more time to run other requests, or comb through our data that gets returned and get it ready to send to the controller. If that is the case, we can create and use our own promise setup with $q. In what we did today with the star wars API, we technically could have done it all within just the $http promise, but it is good to see the setup, and get used to building and resolving your own promises.


### High Level Overview
#### JSON, RESTful, AJAX
- AJAX is the way we make asynchronous calls to a server (ie AJAX request)
- JSON is the format in which the server sends data to the browser, or vica versa.
- REST is a style of architecting and building web services, or API's. You will hear people talk about RESTful API's. "The REST style emphasizes that interactions between clients (browsers) and services (API's) is enhanced by having a limited number of operations (verbs). Because each verb has a specific meaning (GET, POST, PUT and DELETE), REST avoids ambiguity." (http://searchsoa.techtarget.com/definition/REST)

