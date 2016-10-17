# CanvasClock
A JavaScript canvas clocks library for embedding cool clocks in websites

![alt text](https://github.com/Krugaroo/CanvasClock/blob/master/example.PNG  "Example Clocks")

Want to see what I am talking about? A demo can be found on my website here: [http://www.krugaroo.com/#canvasClock](http://www.krugaroo.com/#canvasClock)

## Usage

Using the library is simple (see/run the test.html file it is easy to understand).

First create the canvas object in your page where you want it (it has to be square):
* &lt;canvas id="clock" width="200px" height="200px"&gt;&lt;/canvas&gt;

Second create a configuration object with the options you want, you can leave it empty for the default options:
* object = {};

The following options are possible:
* "indicate": true/false (show indicaters)
* "indicate_color": "#aabbcc" (color of the indicaters)
* "dial1_color": "#aabbcc" (color of the seconds dial)
* "dial2_color": "#aabbcc" (color of the minutes dial)
* "dial3_color": "#aabbcc" (color of the hour dial)
* "time_add": 1/2/3/4 (show the time as well using text)
* "time_add_color": "#aabbcc" (set the color of the text time)
* "time_24h": true/false (use 24 hour notation)
* "timeoffset":0 (modify the time by adding or subtracting seconds to the time)
* "date_add": 1/2/3/4/5 (show the date as well using text)
* "date_add_color": "#aabbcc" (set the color of the date text)
* "bg_color":"#fff" (set the background color)
* "bg_opacity": 0.0-1.0 (set the opacity of the background image if shown)


Call the function of the clock you want to use with the context to the canvas element, size in px and configuration object. After this the clock will be rendering in the canvas element:
* context = document.getElementById('clock1_').getContext('2d')
* clock_conti(context, 200, object);

The following clocks are available (hard to explain, check the link above for the examples):
* clock_conti: A standard analog clock
* clock_digital: A standard digital clock
* clock_norm: A standard analog clock that ticks.
* clock_follow: An analog clock where the dials leaave a trail
* clock_circles: A clock where circles fill up with the time
* clock_grow: An analog clock where the dials grow according to the time
* clock_dots: A clock where time is represented by dots
* clock_num: An analog clock with the time on the dials
* clock_random: A digital clock where the numbers are randomly moved every second
* clock_digitalran: A digital clock where the color changes every second
* clock_bars: A clock that fills up bars as the time increases
* clock_planets: A clock with planets representing the time orbiting around (my favourite)
* clock_roulette: A clock where the numbers slide past.
* clock_reverse: An analog clock that runs in reverse.
* clock_binary: A binary clock.

## Additional functions:

Add a background image to a clock, which will be shown after it is loaded:
* clock_loadBG("img_src",object);

Stop a running clock:
* clock_stop(object);
