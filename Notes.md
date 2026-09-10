Questions I Asked

What does AttributeError: 'AirConditioner' object has no attribute 'fan' mean in Python?
Why am I getting a RecursionError when I set the temperature?
Why doesn't the temperature validation work when I give a value in __init__?
How can I stop cooler() from making the temperature lower than the minimum?

Answer
It means Python is looking for something called fan, but that attribute doesn't exist in my AirConditioner class.
The setter keeps calling itself because I used self.temperature = value inside the temperature setter.
Because I was putting the value directly into _temperature, so Python wasn't using the setter.
I need to check the minimum temperature before decreasing it, or use max() to make sure it never goes below MIN_TEMP.