# CONCEPTS

## Semantic Versioning

Semantic versioning or SemVer is the ideal way of versioning packages. They are usually written like `1.4.5` \(major.minor.patch\)

![Alt Text](https://res.cloudinary.com/practicaldev/image/fetch/s--vTMVK06i--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://thepracticaldev.s3.amazonaws.com/i/uyw4yois1mkqr967ufb8.png)

### _1a._ Bug fix/patch version

Includes bug fixes/documentation spelling mistakes etc.

### _1b._ Minor version

Includes additions of functions or API which does not break anything from the older versions So anything that runs on v1.1.0 should work on v1.9.0 as well.

### _1c._ Major version

Includes version which **breaks stuff**. It can include removing APIs or changing names of functions so anything that works on v1.0.0 may not necessarily work on v2.0.0

### Tilde \(~\) and curret \(^\)

```text
major.minor.patch

1.0.2
```

Major, minor and patch represent the different releases of a package.

npm uses the tilde \(~\) and caret \(^\) to designate which patch and minor versions to use respectively.

So if you see `~1.0.2` it means to install version `1.0.2` or the latest patch version such as `1.0.4`. If you see `^1.0.2` it means to install version `1.0.2` or the latest minor or patch version such as `1.1.0`.

## Programing paradigm

### Functional programming

use function without side-effects, only return the result and combine with another and set as parameter of another function. Avoid changing state or mutation.  
[@FunctionalInterface](https://docs.oracle.com/javase/8/docs/api/java/lang/FunctionalInterface.html) is example of utilizing this paradigm in Java

### Procedural programming

use functions or blocks of code in desired order to build functionality, eg:

```text
void getEntity() {
    verifyUser();
    validateAccess();
    accuireEntities();
    processEntity();
    notifyUser();
}
```

\(is above an antipattern??\)

### Object-oriented programming

functionalities and data are encapsulated into objects. Selection of objects happens in the runtime.

