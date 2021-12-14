# CONCEPTS

## Semantic Versioning

Semantic versioning or SemVer is the ideal way of versioning packages. They are usually written like `1.4.5` (major.minor.patch)

![Alt Text](https://res.cloudinary.com/practicaldev/image/fetch/s--vTMVK06i--/c\_limit%2Cf\_auto%2Cfl\_progressive%2Cq\_auto%2Cw\_880/https://thepracticaldev.s3.amazonaws.com/i/uyw4yois1mkqr967ufb8.png)

### _1a._ Bug fix/patch version

Includes bug fixes/documentation spelling mistakes etc.

### _1b._ Minor version

Includes additions of functions or API which does not break anything from the older versions So anything that runs on v1.1.0 should work on v1.9.0 as well. Backward compatible.

### _1c._ Major version

Includes version which **breaks stuff**. It can include removing APIs or changing names of functions so anything that works on v1.0.0 may not necessarily work on v2.0.0

### Tilde (\~) and curret (^)

```
major.minor.patch

1.0.2
```

Major, minor and patch represent the different releases of a package.

npm uses the tilde (\~) and caret (^) to designate which patch and minor versions to use respectively.

So if you see `~1.0.2` it means to install version `1.0.2` or the latest patch version such as `1.0.4`. If you see `^1.0.2` it means to install version `1.0.2` or the latest minor or patch version such as `1.1.0`.

### Inside-out, outside-in development

\---------------------------> inside-out

model - controller - view

<--------------------------- outside-in

### MMF

Minimal Marketable Feature - has hypothesis to prove using given metrics
