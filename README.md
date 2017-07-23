# Learning-Eve-0.3
j.busby
2017-07-23_0036
~~~
commit
 [#greeting message: "hello old world"]
 
commit
 [#greeting message: "Earthlings arise!"]
 
commit
 [#greeting test: "this is only a test"]

~~~

~~~

search
 [#greeting message]
 
search
 [#greeting test]
 
bind
 [#ui/text text: message]
 
bind
 [#ui/text text: test]
 
~~~

 
~~~
commit
 [#ui/button #increment text: "+1"]
~~~
 
~~~
search 
 event = [#html/event/click element: [#increment]]
 
commit
 [#clicked event]
 
~~~

~~~

search
 how-many = gather/count[for: [#clicked]]
 
bind
 [#ui/text text: "The button has been clicked {{owmany}} times"]
 
~~~


~~~

commit
 [#time #system/timer resolution: 1000]
 [#time2 #system/timer resolution: 4000]
 
~~~



~~~

search
 [#time2 second]
 
bind
 [#ui/text text: second]
 
~~~

~~~
 
search
 [#time second]
 
bind
 [#ui/text text: second]

~~~
