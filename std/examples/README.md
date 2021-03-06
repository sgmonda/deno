# Deno example programs

This module contains small scripts that demonstrate use of Deno and its standard
module.

You can run these examples using just their URL or install the example as an
executable script which references the URL. (Think of installing as creating a
bookmark to a program.)

### A TCP echo server

```shell
deno https://deno.land/std/examples/echo_server.ts --allow-net
```

Or

```shell
deno install --allow-net echo_server https://deno.land/std/examples/echo_server.ts
```

### cat - print file to standard output

```shell
deno install --allow-read deno_cat https://deno.land/std/examples/cat.ts
deno_cat file.txt
```

### catj - print flattened JSON to standard output

A very useful command by Soheil Rashidi ported to Deno.

```shell
deno install --allow-read catj https://deno.land/std/examples/catj.ts
catj example.json
catj file1.json file2.json
echo example.json | catj -
```

### curl - print the contents of a url to standard output

```shell
deno --allow-net=deno.land https://deno.land/std/examples/curl.ts -- https://deno.land/
```

### gist - easily create and upload Gists

```
export GIST_TOKEN=ABC # Generate at https://github.com/settings/tokens
deno install --allow-net --allow-env gist https://deno.land/std/examples/gist.ts
gist --title "Example gist 1" script.ts
gist --t "Example gist 2" script2.ts
```
