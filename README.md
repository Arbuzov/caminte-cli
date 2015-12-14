## CaminteJS CLI

  Command line interface for CaminteJS ORM

### CaminteJS ORM db adapters:
    mysql, sqlite3, postgres, mongodb, redis, riak, couchdb(nano), rethinkdb, tingodb

<table>
    <tr>
      <td><img width="100" src="https://github.com/biggora/caminte/raw/master/media/memory.png"/></td>
      <td><img width="100" src="https://github.com/biggora/caminte/raw/master/media/mongodb.png"/></td>
      <td><img width="100" src="https://github.com/biggora/caminte/raw/master/media/mysql.png"/></td>
      <td><img width="100" src="https://github.com/biggora/caminte/raw/master/media/postgresql.png"/></td>
      <td><img width="100" src="https://github.com/biggora/caminte/raw/master/media/sqlite.png"/></td>
      <td><img width="100" src="https://github.com/biggora/caminte/raw/master/media/mariadb.png"/></td>
      <td><img width="100" src="https://github.com/biggora/caminte/raw/master/media/firebird.png"/></td>   
    </tr>
    <tr>
      <td><img width="100" src="https://github.com/biggora/caminte/raw/master/media/couchdb.png"/></td>
      <td><img width="100" src="https://github.com/biggora/caminte/raw/master/media/rethinkdb.png"/></td>
      <td><img width="100" src="https://github.com/biggora/caminte/raw/master/media/redis.png"/></td> 
      <td><img width="100" src="https://github.com/biggora/caminte/raw/master/media/tingodb.png"/></td>      
      <td><img width="100" src="https://github.com/biggora/caminte/raw/master/media/neo4j.png"/></td> 
      <td><img width="100" src="https://github.com/biggora/caminte/raw/master/media/arangodb.png"/></td>
      <td><img width="100" src="https://github.com/biggora/caminte/raw/master/media/cassandra.png"/></td>
    </tr>
</table>

## Installation

    $ npm install -g caminte-cli

## Quick Start

 The quickest way to get started with caminte is to utilize the executable `caminte(1)` to generate an application as shown below:


 Install dependencies:

    $ npm install

 Edit `./config/index.js` file, to configure the connection to the database server.

 Create model:

    $ caminte -g User name email password desciption:text created:date


### Usage

    $ caminte [options] [dir]

### Options

    -h, --help                  output usage information
    -V, --version               output the version number
    -i, --init <appname>        create caminte sctructure
    -g, --generate <modelname>  generate data model
    -a, --adapter               database adapter (mysql|redis|etc...)
    -f, --force                 force on non-empty directory

### Examples

    # create model
    $ caminte -g Post active:bool name:string desc:text created:date

### Routes

will provide the following routes:

    method        route                    action 
    ------------------------------------------------------------
    GET           /:table                  index      
    GET           /:table/:id              show       
    POST          /:table                  create    
    PUT           /:table/:id              update      
    DELETE        /:table/:id              destroy 

### Directory structure

On initialization directories tree generated, like that:

    .
    |-- bin
    |   `-- www
    |-- config
    |   `-- index.js
    |-- lib
    |   |-- inflection.js
    |   |-- tools.js
    |   `-- xml.js
    |-- models
    |   `-- User.js
    |-- public
    |   |-- css
    |   |   `-- ...
    |   |-- js
    |   |   `-- ...
    |   `-- img
    |       `-- ...
    |-- app.js
    `-- package.json



### Recommend extensions

- [TrinteJS](http://www.trintejs.com/) - Javascrpt MVC Framework for Node.JS
- [CaminteJS](http://www.camintejs.com/) - Cross-db ORM for NodeJS
- [2CO](https://github.com/biggora/2co) - is the module that will provide nodejs adapters for 2checkout API payment gateway.

## License

(The MIT License)
 
Copyright (c) 2014 Aleksej Gordejev &lt;aleksej@gordejev.lv&gt;

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

## Resources

- Visit the [author website](http://www.gordejev.lv).
- Follow [@biggora](https://twitter.com/#!/biggora) on Twitter for updates.
- Report issues on the [github issues](https://github.com/biggora/caminte-generator/issues) page.

[![Analytics](https://ga-beacon.appspot.com/UA-22788134-5/caminte-generator/readme)](https://github.com/igrigorik/ga-beacon) [![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/biggora/caminte-generator/trend.png)](https://bitdeli.com/free "Bitdeli Badge")