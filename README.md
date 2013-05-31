# net-ping

> A collection of classes that provide different ways to ping computers.

## Prerequisites

The win32-open3 (1.8.x) and windows-pr libraries are required on
MS Windows when using the Net::Ping::External class unless you're
using JRuby.

JRuby users should use 1.6.7 or later.

## Installation

    gem install net-ping

## Notes

Please read the documentation under the 'doc' directory. Especially pay
attention to the documentation pertaining to ECONNREFUSED and TCP pings.

Also note the documentation regarding down hosts.

You do not need win32-open3 with Ruby 1.9.x. The open3 library that ships
as part of the Ruby standard library should work.

## How to require net-ping

You can do either this:

```ruby
require 'net/ping'
```

In which case you will get Net::Ping and all of its subclasses. Or,
you can load individual subclasses like this:

```ruby
require 'net/ping/tcp'
```

The former has the advantage of being easier to remember and all inclusive,
not to mention backwards compatible. The latter has the advantage of
reducing your memory footprint.

## Known Issues

Older versions of Ruby 1.9.x may not work with UDP pings.

Older versions of JRuby will return false positives in UDP pings
because of an incorrect error class being raised. See JRuby-4896.

JRuby 1.6.7 or later is required for external pings because of a bug
in earlier versions with open3 and stream handling.

## License

Artistic 2.0

## More documentation

If you installed this library via Rubygems, you can view the inline
documentation via ri or fire up 'gem server', and point your browser at
http://localhost:8808.
