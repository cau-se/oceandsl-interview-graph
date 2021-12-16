# OceanDSL Interview Graph

We conducted several interviews in context of the OceanDSL project
to understand the socio-technical domain of ocean modelling and
the research and development processes. We analyzed the interviews
with a Thematic Analysis approach. One ouput of this approach is
a thematic map containing codes and themes. We also included 
categories in this graph as 'sub-themes' to better handle the
complexity of the analysis.

This git-project contains the raw data of the thematic map and
the necessary files to view them in a web browser. Unfortunately,
a web browsers block access from HTML files to other files on the
local machine for security reasons. Therefore, we bundled our
view and data files with a Docker setup which makes is fairly
easy to run on any machine as a small web server. Below we
describe how these files can be used either with an existing
web server or our Docker image.

## Docker based Setup

Clone the content of the repository:

```git clone https://github.com/cau-se/oceandsl-interview-graph.git```

Change to the `oceandsl-interview-graph` directory.

```cd oceandsl-interview-graph```

Build the docker image with the name `ta-oceandsl` (of course you
can choose another name):

```docker build -t ta-oceandsl .```

Run docker image (make sure to use the same name here):

```docker run -dit --name my-running-app -p 8080:80 ta-oceandsl```

Access the thematic map in the browser with:

http://localhost:8080/graph.html

## Using existing Web Server Setup

Either your setup of the webserver provides a user based `public-html`
directory, then you can place the content of the graph directory there,
or you copy the content the the web server document folder, e.g.,
`/usr/apache2/htdocs/`. Please note that the directories may be
different on your machine. Place all three files from the `graph`
directory of the repository in one location then all should work
perfectly.

