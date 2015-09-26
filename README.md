# OutbackSerial
This is a collection of objects to read and parse data from the serial port of the Outback Mate, a solar system controller, which manages several components of the system, i.e. the inverter, the charge  controller and the battery manager. This code is for the Mate 2, which is a 2010 vintage device. The goal of this code is to make the data from the various components available on a Unix Domain Socket, so other services, e.g. apache, could read them in real time. Another component is to accumulate the inverter energy over time and write the energy output to a MySql database. This code is rather unrefined, but seemed to work more or less reliably in my power monitor application. The most common source of error is the serial communication which fails a couple hundred times over a day - probably due to it being called  86400 times and the use of 7 m long serial cable.