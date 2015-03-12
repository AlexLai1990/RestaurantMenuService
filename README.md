## Restaurant Menu Service

This is a simple web application to represent information of restaurants, menus in the remote Database.
Users can have webUI to do CRUD for restaurants and menus.

The server is implement in Python with Flask Framework, the Database is using sqlite with SQLAlchmey ORM to manipulate data.
The front-end is using bootstrap and JQuery to do some UI stuffs.

The application is still Ongoing to make a Menu Order System for customers.

Demo Link:
	
	*  http://whispering-refuge-1911.herokuapp.com/


## Deploy app on Heroku: 

1.	Register an account, install Heroku/ git

2.	Prepare application in local folder or from git repository (It needs the additional file to set up in the remote server: requiremnts.txt/ Procfile.txt/ runtime.txt)

3.	Enter the app folder

		a)	heroku create   -> before we deploy in the server, we can use “foreman start web” , this will do the exact thing in server.
	
		b)	git push heroku master
	
		c)	heroku ps:scale web=1       -> this is to make sure the instance in server is running
	
		d)	heroku open  -> auto open in chrome.


Note : 
* How to create requirements.txt?
	
	Pip freeze >! requirements

* How to create Procfile?

	In Heroku, the server will allocate dynamic port for your application.

	In Procfile:

	web: python ./Flask_Test/first_flask.py runserver 0.0.0.0:$PORT

And in app.py:
    port = int(os.environ.get('PORT', 5000))
    app.run(host = '0.0.0.0', port = port)

* How to create runtime.txt?


	type "python-2.7.5" in the runtime.txt


### Ref: 

https://www.udacity.com/course/ud088 

http://virantha.com/2013/11/14/starting-a-simple-flask-app-with-heroku/

https://devcenter.heroku.com/articles/getting-started-with-python#deploy-the-app

