## AJAX Panel for Grafana

The AJAX Panel can load external content into the dashboard.  This is a more powerful and flexible solution than
using an <iframe 


### Options

- **Method**:

  GET or POST or iframe

- **URL**:

  The URL to request

- **Parameters**:

  The parameters that will be passed in the request.  This is a javascript object with access to the variables:
  	- `ctrl` The control object.
  
  Sample Parameters:
	```
	{
	 from:ctrl.range.from.format('x'),  // x is unix ms timestamp
	 to:ctrl.range.to.format('x'), 
	 height:ctrl.height
	}
	```


### Screenshots

- [Screenshot of the options screen](https://raw.githubusercontent.com/ryantxu/ajax-panel/master/src/img/screenshot-ajax-options.png)

#### Changelog


##### v0.0.4 (not released yet)

- Support template variables in parameters (@linar-jether)
- Improved error handling
- Move ajax requests to 'issueQueries' block rather than refresh
- Show loading spinner


##### v0.0.3

- Support template variables in url (@linar-jether)
- Adding iframe method (@linar-jether)


##### v0.0.2

- Quick and Dirty, but it works!



### Wishlist... if you are looking for a project :)
 - Add authentication info to the sub-request?
 - Configure timer to refresh
 - Load CSS file?
 - configure javascript for display
 - Check that parameters have changed before sending a new request
