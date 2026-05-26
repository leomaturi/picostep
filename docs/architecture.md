# Architecture

PicoStep is organized around neutral numerical containers and explicit physical roles.

`Field` represents data on a structured grid.  
`State` and `Parameter` define the role of that data inside a problem.  
`Model`, `Stepper`, `Operator`, `Observable` and `Writer` remain separated to keep the code modular and extensible.