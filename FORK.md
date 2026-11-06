# Fork notes

Fork of [SteeleDesmond/sample.mono-to-ms.pbw-monolith](https://github.com/SteeleDesmond/sample.mono-to-ms.pbw-monolith),
kept for the MonoSplit study (decomposition of Java monoliths into microservices).

Branch `monosplit` starts at commit `e6f2a6a437221c2652b907a709cf0343780013f2`, the version
used in the literature (MonoEmbed, Sellami and Saied, 2025). The tag `monosplit-pin` marks
that unchanged commit.

Changes on the branch, build only:

- `pom.xml`: maven-compiler-plugin `source`/`target` from 1.6 to 1.8, because JDK 9 and
  later no longer compile for Java 6. Java 8 class files hold the same invocations, so the
  static call graph is the same.

No Java source, resource or dependency was changed: `git diff e6f2a6a -- '*.java'` is empty.
