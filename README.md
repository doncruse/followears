# Followears 

This is a simple webapp, designed to be used from an iPhone, to quickly see which of your Twitter followers will overhear an @ reply that you direct to someone else.

## Background

I wrote the first version of this little Sinatra app in 2010. At a meeting of Austin on Rails, we had two speakers &mdash; one discussing how to use memcache to speed up an application's internal calls, and the other speaker discussing the Twitter API.  I was already familiar with this problem of trying to pin down the scope of @ replies, which caused me to hesitate (sometimes) before sending one out.. I had recently learned just enough Sinatra to be dangerous, so that became the framework.

## The Big Refactor

**NOTE:** The app has not yet been updated to fit the most recent Twitter API. Some refactoring can be done before that time, especially built around real tests. But fixing the API seems like an important early step.

Inspired by attending Lone Star Ruby Conference in 2013, I've decided to revive this project to work on some refactoring techniques.  The project is open source (MIT license), and I also hope to do at little pair programming along the way. I enjoyed using this app before it broke with the Twitter API. I'd like to bring it back to life.

The version of the code that exists in July 2013 is procedural. It does not define custom classes and uses a module just to shift the location of related code. The code simply walks through the steps of accessing the APi. The "math" of doing the needed set computations was done very naively. (It should perhaps be rewritten to use something like Redis, which has native set operations.) And there are no tests. Not a one.

The original (2010) version of the code is available here: https://github.com/doncruse/twitears-app

# The MIT License

*Copyright (c) 2010-2013 Don Cruse*

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
