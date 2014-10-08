# Docker image with Node.js and Ruby

Includes:

- nodejs
- ruby
- supervisor
- git
- bower
- grunt
- yo
- pg
- karma
- compass

Edit the config/supervisord.conf file if you need to and then override the /etc/supervisor/conf.d directory, by default it will run grunt serve.

To use it, install [Fig](http://fig.sh) and then create the following fig.yml file

    web:
      image: luis/nodejs-ruby
      ports:
        - "3000:3000"
      volumes:
        - ./:/var/www
        - /var/log/docker:/var/log/supervisor
      environment:
        NODE_ENV: development

## License
The MIT License (MIT)

Copyright (c) <year> <copyright holders>

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