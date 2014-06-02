fintp_transport
===============

Message-oriented middleware access library for **FinTP**

Requirements
------------
- Boost
- pthread
- ActiveMQ-CPP
- IBM WebSphere MQ client
- **fintp_utils**
- **fintp_log**

Build instructions
------------------
- On Unix-like systems, **fintp_transport** uses the GNU Build System (Autotools) so we first need to generate the configuration script using:


        autoreconf -fi
Now we must run: 

        ./configure [--with-activemqcpp=yes/no][with-wmq=yes/no/path]
        make
By default, **fintp_transport** is built with ActiveMQ-CPP support and no WebSphere MQ support.
- For Windows, a Visual Studio 2010 solution is provided.

License
-------
- [GPLv3](http://www.gnu.org/licenses/gpl-3.0.html)

Copyright
-------
COPYRIGHT.  Copyright to the SOFTWARE is owned by ALLEVO and is protected by the copyright laws of all countries and through international treaty provisions. 
NO TRADEMARKS.  Customer agrees to remove all Allevo Trademarks from the SOFTWARE (i) before it propagates or conveys the SOFTWARE or makes it otherwise available to third parties and (ii) as soon as the SOFTWARE has been changed in any respect whatsoever. 
