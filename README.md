makemeasandwich.js
==========================
This is a Node.js application that is capable of ordering a Jimmy John's sandwich via command line, bringing to life this legendary XKCD comic.

![](http://imgs.xkcd.com/comics/sandwich.png)

It does this through the combination of Node.js + PhantomJS along with some other command line prompt tools that makes ordering a sandwich even more freaky fast.

Installation
---------------------------
To install this application on your computer, you can simply use NPM to install it as a global command.

```
npm install -g makemeasandwich
```

Usage
---------------------------
To run this command, simply type it in your terminal.

```
makemeasandwich
```

Or, if you want to stay true to the comic...

```
sudo makemeasandwich
```

This will then walk you through the login process, as well as sandwich selection process, and even checkout... all through the command line.  You can also provide configurations to make each order super simple.  This is done via a JSON file that you can pass into the application using the ```o``` argument like so.

```
sudo makemeasandwich -o order.json
```

This order json file looks like the following...

```
{
    email: 'me@example.com',
    sandwich: {
        name: 'Country Club',
        no: [
            'tomatoes',
            'lettuce'
        ],
        add: [
            'mayo'
        ],
        other: [
            'cut in half'
        ]
    },
    charge: {
        name: 'My Visa'
    }
}
```

The charge settings are simply the pre-defined credit card settings that Jimmy Johns already keeps for you in their system.  The first time you create an order, you will need to put in your credit card information which it will simply prompt you for it.