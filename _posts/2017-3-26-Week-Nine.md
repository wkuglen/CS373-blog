---
layout: post
title: Week 9
---

### What did you do this past week?
This week was the first week back from Spring Break. In class we finished talking about the mechanics of C++ classes and discussed friend functions. Project 3: Allocator was due on Friday (it was originally due Thursday, but there were some mistakes in the HackerRank solutions).

### What's in your way?
Since there are no projects this week, I need to get on a machine and practice C++. On the past few quizzes, I have missed questions relating to concepts that we saw in class. I think practicing C++ would help me solidify those concepts by allowing me to see them for myself.

### What will you do next week?
Next week, marks the start of my second round of midterms. I will also start Project 4 whenever it is announced this week.

### What's my experience of the class?
This week was a fairly typical week for class. For Project 3, there was an error with the tests on HackerRank that caused correct solutions to fail. As a result the project due date was moved from Thursday to Friday, which I thought was fair. The change only affected a small part of our code so it was simple to fix. This project was also the earliest I have finished a project since my partner and I worked on it steadily rather than procrastinating.

### What's my pick-of-the-week or tip-of-the-week?
My tip-of-the-week is to use color when using print statements for debugging. Through [ANSI escape codes](https://en.wikipedia.org/wiki/ANSI_escape_code#Colors) you can easily add color to text that is printed out to the terminal (at least on Linux and macOS/Mac OS X). You can use these codes to differentiate visually between methods and/or variables. Here are some common examples:

{% highlight C++ %}
//Line 1
std::cout << "\x1b[31m" << "This is RED text!" << "\x1b[0m" << std::endl;

//Line 2
std::cout << "\x1b[32,1m" << "This is BOLD GREEN text!" << "\x1b[0m" << std::endl;

//Line 3
std::cout << "\x1b[43m" << "This text is highlighted YELLOW!" << "\x1b[0m" << std::endl;
{% endhighlight %}

The codes seem odd but follow a simple pattern: They all start with `"\x1b["` and end with `"m"`. Numbers 30 to 37 represent the text color (such as in Line 1 above). Numbers 40 to 47 represent the background (a highlight) color (such as in Line 3 above). The number 1 makes the text bold and the number 0 clears all of the formatting. These codes can be chained by a comma between numbers (such as in Line 2 above) and will persist until they are cleared by a 0. Here is a simple chart showing the color codes:

| Color | Foreground | Background |
| --- | --- | --- |
| BLACK | `"\x1b[30m"` | `"\x1b[40m"` |
| RED | `"\x1b[31m"` | `"\x1b[41m"`|
| GREEN | `"\x1b[32m"` | `"\x1b[42m"`|
| YELLOW | `"\x1b[33m"` | `"\x1b[43m"`|
| BLUE | `"\x1b[34m"` | `"\x1b[44m"`|
| MAGENTA | `"\x1b[35m"` | `"\x1b[45m"`|
| CYAN | `"\x1b[36m"` | `"\x1b[46m"`|
| WHITE | `"\x1b[37m"` | `"\x1b[47m"`|

And here are the special formatting codes:

| Format | Code |
| --- | --- |
| BOLD | `"\x1b[1m"` |
| CLEAR | `"\x1b[0m"` |
