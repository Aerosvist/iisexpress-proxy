## iisexpress-proxy
[![NPM version][npm-image]][npm-url]
[![Dependency Status][david-image]][david-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

Simple command-line utility for .NET developers looking to test web applications served by IIS Express on remote devices.

## Motivation
Are you a .NET developer building mobile web application?
Have you ever been frustrated by the fact that [there's no easy way](https://www.google.com/search?q=iis+express+remote+access) to enable IIS Express to accept connections from remote devices?...

## Installation
Most likely you'll want **iisexpress-proxy** installed as a global module:

    npm install -g iisexpress-proxy

Note: *You need to have [Node.js](https://nodejs.org/) installed.*

## Usage
If you installed **iisexpress-proxy** as a global module:

    iisexpress-proxy localPort to proxyPort

For instance, if your application is running on IIS Express on port 51123, run:

    iisexpress-proxy 51123 to 3000

The program will list the external addresses you can use for testing your application on remote devices.

![iisexpress-proxy](https://raw.github.com/icflorescu/iisexpress-proxy/master/diagram.jpg)

## How does it work
It's proxying the HTTP traffic on `http://localhost:localPort` to `proxyPort` on all the available network interfaces and it's also [changing the origin of the host header to localhost](https://github.com/nodejitsu/node-http-proxy/blob/master/lib/http-proxy.js#L43), allowing you to test web applications hosted by IIS Express on various remote devices (mobile devices, other desktops, etc.).

## Credits and attributions
This command-line utility is a simple wrapper around [http-proxy](https://github.com/nodejitsu/node-http-proxy).
The original [http-proxy](https://github.com/nodejitsu/node-http-proxy) logo was created by [Diego Pasquali](http://dribbble.com/diegopq). Elements from a [business vector designed by Freepik](http://www.freepik.com/free-photos-vectors/business) were used in the above diagram.

## Endorsing the author
If you find this piece of software useful, please [tweet about it](http://twitter.com/share?text=Checkout%20iisexpress-proxy%20-%20the%20simple%20way%20to%20access%20your%20IIS%20Express%20applications%20from%20remote%20devices!&url=https%3A%2F%2Fgithub.com%2Ficflorescu%2Fiisexpress-proxy&hashtags=iisexpress%2Cremote%2Cvisualstudio%2Cnode.js%2Cjavascript&via=icflorescu) and endorse me on LinkedIn:

[![Ionut-Cristian Florescu on LinkedIn](https://static.licdn.com/scds/common/u/img/webpromo/btn_viewmy_160x25.png)](https://www.linkedin.com/in/icflorescu)

[npm-image]: https://img.shields.io/npm/v/iisexpress-proxy.svg?style=flat-square
[npm-url]: https://npmjs.org/package/iisexpress-proxy
[david-image]: http://img.shields.io/david/icflorescu/iisexpress-proxy.svg?style=flat-square
[david-url]: https://david-dm.org/icflorescu/iisexpress-proxy
[license-image]: http://img.shields.io/npm/l/iisexpress-proxy.svg?style=flat-square
[license-url]: LICENSE
[downloads-image]: http://img.shields.io/npm/dm/iisexpress-proxy.svg?style=flat-square
[downloads-url]: https://npmjs.org/package/iisexpress-proxy
