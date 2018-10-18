## Core Erlang

<a>
  <img src="https://github.com/stan-alam/erlangOTP/blob/develop/erlang/01/svg_files/erlang-0.svg" width="80%" height="80%">
</a

<a>
  <img src="https://github.com/stan-alam/erlangOTP/blob/develop/erlang/01/svg_files/erlang-1.svg" width="80%" height="80%">
</a

## Erlang OTP

## Intro

erlang OTP for implementing fault-tolerant, scalable, soft real-time system with requirements for high availability.


Event-driven -- reacts to stimuli, load and responds to failure == "responsive"


Which all depends on the middleware provided in the earlang ecosystem. i.e availability and scalability, concurrency.

**OTP** is a domain-independent set of frameworks, principles that guide and support the structure, implementation, and deployment of **erlang**
systems. Use OTP in your projects with Erlang, avoid the headaches.

OTP is consists of 3 building blocks which in combination are used together to provide a solid approach to
designing and developing systems in the main problem domain of **fault-tolerant, scalable, soft real-time system with requirements for high availability.**

OTP is erlang the tools and libraries and set of design of principles.


## Erlang + Tools/libraries + System design principles = OTP

Open Telecom platform


The first building block is erlang itself. This includes the semantics of the language it's underlying virtual machine.
Key language features such as lightweight processes, lack of shared memory and async message passing. The monitors and error reporting
allow to build with relative ease, and complex suprvision hierarchies with built-in fault recovery.

**Messaging passing and error propagation are async, the semantics and logic of a system that is developed to run in a single Erlang node can be easily distributed without having to change any of the code base.**

Significant difference between running on a single node and running in a distributed environment is the latency with which the messages and errors
are delivered. But in soft-real time systems, you have to consider latency regardless of whether the system is distributed or under heavy load.
By solving the latter you have solved both.


**Tools and libs**

basic apps include

(erts) The Erlang runtime system

The kernal

the standard libs (stdlib)

the System architecture support libs (SASL)

This is the bare bone to do anything meaningful

* Database mnesia -- distributed database and odbc an interface to to interact with relational SQL databases.
  Mnesia is accessed through the erlang API

 * Operations and maintenance applications include **os_mon**, an application that allows you to monitor
 the underlying operating system, snmp, a **Simple Network Management Protocol** agent and client; and otp_mibs,
 management information bases that allow to manage Erlang systems using **SNMP**

The *debugger* is a graphical tool allow to step through code while influencing the state functions.

The *observer* integrates the application monitor and the process manager, alongside basic tools to monitor
your erlang systems as they are developed and in prod.

The **dialyzer** is a static analyzer that finds type discrepancies, dead code and other issues.

The event tracer (et) uses ports to collect trace events in distributed environments and *percept* allows
to locate bottlenecks in your system by tracing and visualizing concurrency-related activities.


Generic behaviors that are part of OTP middleware :

	* Generic servers, providing a client-server design pattern

	* Generic finite state machines, allowing to implement FSMs
