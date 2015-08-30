## About Glimpse 
Glimpse is a super simple server vital starts service written in bash. There are many much more involved services out there, such as ``collectd`` for instance. However, I needed something really simple to show very basic server stats in the today widget on OSX, so I made glimpse.

Hope someone else will also find it useful.

## Installing Glimpse

The only prerequisite of glimpse that you may not have on a standard linux system is the ``socat`` utility necessary for ``glimpsed``. To install it just run ``apt-get install socat`` or ``yum install socat`` or similar install command for your system.

After this, just copy ``glimpse`` and ``glimpsed`` into a folder on your system and start it by running ``glimpsed``.

## Using Glimpse

Now that the glimpse server is running, simply go to http://server-ip:5488/ to see the server stats. You can change the port number by editing the ``glimpsed`` file.

To look at the server stats from another command line, simply run ``curl http://server-ip:5488/``.

In my case I wanted to use it with the wonderful [Today-Scripts](https://github.com/SamRothCA/Today-Scripts). Grab the Today Scripts widget, install it, and add ``curl http://server-ip:5488/`` as one of your scripts. Now you have some basic server stats in the today side bar.

## Final Thoughts

Released under MIT License. Fork and enjoy!