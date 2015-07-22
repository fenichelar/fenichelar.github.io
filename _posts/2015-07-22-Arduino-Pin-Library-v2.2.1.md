---
layout: post
title: Arduino Pin Library Version 2.2.1
---

I have updated my Arduino Pin library; it is now capable of simultaneous operations on multiple Pins. The library is used for fast digital I/O using port manipulation supporting the Arduino Mega, Arduino Uno, and Arduino Leonardo. The source code can be found at [https://github.com/fenichelar/Pin](https://github.com/fenichelar/Pin). Complete documentation can be found at [https://fenichelar.github.io/Pin](https://fenichelar.github.io/Pin). The library is also avaliable on the Arduino Library Manager. Here are some examples of the new features:

#Simultaneous Operations on Multiple Pins
All Pins in array must use the same DDR and PORT registers. Look at the corresponding file in the boards directory to determine what register each pin uses.

Import Pin Library with support for simultaneous operations
{% highlight c++ %}
#include <Pin.h>
#include <PinGroup.h>
{% endhighlight %}
Create array of Pins for simultaneous operations
{% highlight c++ %}
Pin myPinGroup[] = {2,3,5};
{% endhighlight %}
Simultaneously set mode for array of Pins to input
{% highlight c++ %}
setInput(myPinGroup);
{% endhighlight %}
Simultaneously set mode for array of Pins to output
{% highlight c++ %}
setOutput(myPinGroup);
{% endhighlight %}
Simultaneously check if array of Pins are all HIGH
{% highlight c++ %}
getValue(myPinGroup) == HIGH
{% endhighlight %}
Simultaneously check if array of Pins are all LOW
{% highlight c++ %}
getValue(myPinGroup) == LOW
{% endhighlight %}
