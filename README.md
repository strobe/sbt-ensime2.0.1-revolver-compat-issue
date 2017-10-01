~/.sbt/0.13/plugins/plugins.sbt

```
addSbtPlugin("org.ensime" % "sbt-ensime" % "2.0.1")
```

~/.sbt/0.13/global.sbt

```
import org.ensime.EnsimeKeys._

cancelable in Global := true
```

sbt output:

```
[info] Loading global plugins from /Users/evgeniy/.sbt/0.13/plugins/project
[info] Loading global plugins from /Users/evgeniy/.sbt/0.13/plugins
[info] Loading project definition from /Users/evgeniy/tmp/sbt-ensime2.0.1-revolver-compat-issue/project
[info] Compiling 1 Scala source to /Users/evgeniy/tmp/sbt-ensime2.0.1-revolver-compat-issue/project/target/scala-2.10/sbt-0.13/classes...
[error] /Users/evgeniy/tmp/sbt-ensime2.0.1-revolver-compat-issue/project/Dependencies.scala:1: package sbt contains object and package with same name: compat
[error] one of them needs to be removed from classpath
[error] import sbt._
[error]        ^
[error] /Users/evgeniy/tmp/sbt-ensime2.0.1-revolver-compat-issue/project/Dependencies.scala:4: value %% is not a member of String
[error]   lazy val scalaTest = "org.scalatest" %% "scalatest" % "3.0.3"
[error]                                        ^
[error] two errors found
[error] (compile:compileIncremental) Compilation failed
Project loading failed: (r)etry, (q)uit, (l)ast, or (i)gnore?
```
