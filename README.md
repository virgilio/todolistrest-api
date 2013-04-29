todolistrest-api
================

Play framework RestAPI for a todo list. To deploy with play, just go to root directory and run 
$ play start <port> 
or to start on a random port just run
$ play run 

To deploy with SBT
$ sbt compile
$ sbt "start <port>" 

or to a random port for tests purposes
$ sbt run 


# Basic REST
============
GET     /tasks                controllers.Application.tasks()
OPTIONS /tasks                controllers.Application.checkPreFlight
POST    /tasks                controllers.Application.newTask()
POST    /tasks/:id/delete     controllers.Application.deleteTask(id: Long)
POST    /tasks/:id/update     controllers.Application.updateTask(id: Long)

# Goodies
=========
POST    /tasks/:id/done       controllers.Application.taskDone(id: Long)
POST    /tasks/:id/open       controllers.Application.taskOpen(id: Long)

