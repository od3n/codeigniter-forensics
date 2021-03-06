# Forensics for CodeIgniter

Forensics is a high-powered, completely customizable replacement for the CodeIgniter Profiler.

## What's New?

Forensics adds a few things to the stock Profiler that should make your life as a developer a bit easier. At least when it comes to debugging.

- The Profiler output is now completely skinnable. If you've read the comments in the Profiler class before, this is something that the EllisLab devs have said for a while it would be nice to do. Congrats. It's done. 
- The output now also includes a list of all files that your CodeIgniter app includes, as well as their location (relative to your FCPATH).
- Output also has the ability to log items and track memory in your project via a new console class. 
- Any variables sent to the view are shown in the bar.

The default look, and some of the additional functionality, was heavily inspired by ParticleTree's [PHP Quick Profiler](http://particletree.com/features/php-quick-profiler/).

## Installing

Forensics is intended to be installed as a [Spark](http://getsparks.org). Please see their site for more information.

## Forensics Logging

In addition to the normal information that CI's Profiler provides, you now have two new logging commands at your disposal that work with the Forensics Profiler:

### Console::log($data) 

This function accepts any data type and simply creates a pretty, readable output of the variable, using print_r(). Very handy for logging where you are in the script execution, or outputting the contents of an array, or stdObject to your new 'console'.

### Console::log_memory($variable, $name)

The log_memory function has two uses.

1) When no parameters are passed in, it will record the current memory usage of your script. This is perfect for watching a loop and checking for memory leaks.

2) If you pass in the $variable and $name parameters, will output the amount of memory that variable is using to the console.

In order to use either of these functions, you must be sure to load the Console library before you use it.

## Other Tips

You can change the location of the profiler bar by changing the `$bar_location` variable at the top of the *profiler_template* view to one of the following locations: 

* top-right
* top-left
* bottom-left
* bottom-right
* top
* bottom
