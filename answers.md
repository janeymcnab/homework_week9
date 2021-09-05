What does the directory structure look like?

events_app
/app/templates
    event_list.hmtl
/controllers
    controller.py
/models
    event.py
    events.py
/static/css
    main.css
/templates
    base.html
    index.html
/flaskenv
/app.py


What are the different parts that make up the app?
Templates, controllers, models, the static file.


What are controllers responsible for?
A controller deals with requests. It accepts input from the user and then determines what functions are run.

What are templates responsible for?
Templates are used when lots of pages share elements (like nav bars) and mean that the developer doesn't have to build each of those pages by hand. This is good as it means that code doesn't have to be repeated. 

What is the static folder for?
The static folder contains assests used by templates - in this case the CSS file. When those assests are modified, it only has to be changed once - in the static folder.

How do you think we will combine what we've done this week with Flask?
The work that we've done this week with databases will combine with the MVC model by interacting with the "models". In the model a database can be defined. 


How do you create a route in the controller?
A route acts as an index. When a route is selected a request for that page is sent to the server, and that page is returned to the user.
In this instance - an example of a route is created by the following code:

from app import app

@app.route('/events')
def index():
    return render_template('index.html', title='Home', events=events)


The models/events.py file acted as some dummy data for our app. This will no longer be necessary. Why is that the case?

The dummy data is useful initially as it allows the developer to see that the page is working correctly. But in production a user would want to enter their own data. 
