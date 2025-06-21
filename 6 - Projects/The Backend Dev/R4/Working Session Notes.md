- read up on mvc design pattern
	- controller layer routes request to service
	- model behind that (pure data representation)
		- i.e. bank -> number, balance, history, ID, etc.
	- services manipulate model, controller renders a view
	- separation between data, view, and routing behind it
	- differentiation of 'controller' in springboot ("has hijacked")

martin fowler's MVCVM
- for every view theres a model for the view
- one data object per view
- view does not amalgamate data in any way

convention utilization evolves the tooling by baking it in


github actions via .yml

Coding/programming styles (peep martin fowler for potential blog on this and effective java book)
- procedural
	- data lives with the caller
- oo
	- 
- functional
	- 

style types
- functional vs imperitive
- fluence api


code cohesion metric, related should be close together in the file system, unrelated far


data folder -> cross disciplinary data ... not desireable

walk through your code in a debugger to make sure it is correct

https://projectlombok.org/ -> to learn boilerplate, getters etc. (learn annotation)

patterns

code start with controllers
sanitation and validation
if task required of endpoint is simple, might see full implmementation of the controller method in the implmentation
- might just call dao
if complicated will call do service class
- to have whatever logic in controller in once place
controller should do validation, with "valid looking data"

dao -> data access object
- layer closest to database
- takes parameters, calls db, return java object as result to whatever called it
	- might do some joining of data to alleviate the service from doing so
- makes the structure transparent
	- hide the fact that multiple databases are being queried?


JAVA strong typing

python self -> java its implicit
- this keyword is implicit with whatever you write

java resolution scans up to see if local def to see if variable is param, then class, 


action items:
pick a page and learn the db queries
get stronger with java syntax s.t. reading code gets easier
partners page
