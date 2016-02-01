# Markdown Server
[![Build Status](https://travis-ci.org/superzadeh/MarkdownServer.svg?branch=master)](https://travis-ci.org/superzadeh/MarkdownServer)

A simple HTTP server that serves markdown files.

## Usage
Install dependencies, then start the server.
```
git clone https://github.com/superzadeh/MarkdownServer 
cd MarkdownServer
npm install
npm start
```

Drop files in the ./markdown folder, and access them by file name without the extension. 
```
http://localhost:3000/example
```
 
## Hosting on IIS
 
This server comes with a preconfigured web.config file as well as an issnode.yml. To host this site in IIS:
 * Clone/copy the content of this repo in a IIS WebSite.
 * Install [iisnode](https://github.com/tjanczuk/iisnode)
 * Make sure you application's pool identity has read/write permissions to the site's folder
 * The application pool can be in .NET 2 and does not need to enable 32 bits applications
 * Run `npm install` to install dependencies
 * Customize the default `web.config` (enable authentication, etc.)
 * Customize the default `issnode.yml` file (disable dev errors, etc.)

## Configuration

By default, all files within the folder ./markdown will be served. This folder can be changed by 
setting the environment variable `MARKDOWN_FOLDER`.

## Contributions
Pull requests are welcome, as long you keep this thing simple. I want it to be and remain a very 
simple solution to serve markdown files.
