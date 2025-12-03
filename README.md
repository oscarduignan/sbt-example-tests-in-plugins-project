# SBT Example of writing some tests on code in the build scope in the plugins project in `./project` directory

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

If you want to run the plugins tests first, you can use "reload return" to go back to the main project

```
sbt "reload plugins" test "reload return" test
```

Gives something like this if both tests pass, or will stop after first failure if project fails:

<img width="2140" height="612" alt="CleanShot 2025-12-03 at 10 15 48@2x" src="https://github.com/user-attachments/assets/a522104a-a78f-4b0d-a195-638e6200c94d" />
