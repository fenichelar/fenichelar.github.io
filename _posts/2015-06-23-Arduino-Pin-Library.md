---
layout: post
title: Arduino Pin Library
---

I created an Arduino library for fast digital I/O using port manipulation supporting the Arduino Mega, Arduino Uno, and Arduino Leonardo. The source code can be found at [https://github.com/fenichelar/Pin](https://github.com/fenichelar/Pin). Complete documentation can be found at [https://fenichelar.github.io/Pin](https://fenichelar.github.io/Pin). The library is also avaliable on the Arduino Library Manager. Here are so common uses:

## Import Pin Library
{% highlight c++ %}
#include <Pin.h>
{% endhighlight %}

## Create Pin Object
Single Pin
{% highlight c++ %}
Pin myPin = Pin(5);
{% endhighlight %}
Array of Pins
{% highlight c++ %}
Pin myPins[] = {6,7};
{% endhighlight %}

## Use as Input
Set Mode to Input
{% highlight c++ %}
myPin.setInput();
{% endhighlight %}
Enable/Disable Pullup Resistor
{% highlight c++ %}
myPin.setPullupOn();
{% endhighlight %}
{% highlight c++ %}
myPin.setPullupOff();
{% endhighlight %}

## Use as Output
Set Mode to Output
{% highlight c++ %}
myPin.setOutput();
{% endhighlight %}
Set HIGH/LOW
{% highlight c++ %}
myPin.setHigh();
{% endhighlight %}
{% highlight c++ %}
myPin.setLow();
{% endhighlight %}

## Get Pin Info
Get Mode (INPUT/OUTPUT)
{% highlight c++ %}
myPin.getMode();
{% endhighlight %}
Get State (HIGH/LOW)
{% highlight c++ %}
myPin.getState();
{% endhighlight %}
Get Value (HIGH/LOW)
{% highlight c++ %}
myPin.getValue();
{% endhighlight %}

## Toggle
Toggle Mode (OUTPUT -> INPUT, INPUT -> OUTPUT)
{% highlight c++ %}
myPin.toggleMode();
{% endhighlight %}
Toggle State (HIGH -> LOW, LOW -> HIGH)
{% highlight c++ %}
myPin.toggleState();
{% endhighlight %}