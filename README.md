# example

Run all the tests

```
sbt test "reload plugins" test
```

> `reload plugins` puts you into the plugins project `project/` so after that the subsequent test executes the tests in there.
>
> https://www.scala-sbt.org/1.x/docs/Plugins.html#1c%29+Automatically+managed%3A+command-line+approach

And to show that stuff in project/Example.scala is accessible to build.sbt I replaced the project name with `Example.author` so if you run this:

```
scala "show name"
```

you should see some output followed at the end by:

```
[info] Oscar Duignan
```
