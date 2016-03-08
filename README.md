Heroku buildpack: FFMpeg + x264 + Ogg Vorbis
=======================

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) for using [ffmpeg](http://www.ffmpeg.org/) in your project.  
It doesn't do anything else, so to actually compile your app you should combine it with a real buildpack.

Usage
-----
To make it work with Ruby (Rails) buildpack do:

    $ heroku buildpacks:add https://github.com/heroku/heroku-buildpack-ruby
    $ heroku buildpacks:add https://github.com/znupy/heroku-buildpack-ffmpeg-x264-ogg
    $ git push heroku master
    ...

You can verify installing ffmpeg by following command.

    $ heroku run "ffmpeg -version"

Hacking
-------
If you want to use your own ffmpeg binary, fork and rewrite following line.

https://github.com/shunjikonishi/heroku-buildpack-ffmpeg/blob/master/bin/compile#L10
