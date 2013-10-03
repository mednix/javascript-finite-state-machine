Javascript Finite State Machine
===============================
Usage
-----
Create a new Finite State Machine  Object (FSM):
var fsm=FiniteStateMachine.create({
	events:[
		{name:"getReady", from:"green" , to:"orange"},
		{name:"stop", from:"green" , to:"red"},
		{name:"stop", from:"orange" , to:"red"},
		{name:"pass", from:"orange" , to:"green"},
		{name:"getReady", from:"red" , to:"orange"},
		{name:"pass", from:"red" , to:"green"}
	]
});
will create an object with a method for each event:
fsm.getReady()
fsm.stop()
fsm.pass()
and with following members:
fsm.current() return the current state
fsm.is(state) test if state is the current
fsm.can(event) test if event can be fired for the current state
