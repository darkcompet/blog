# Mono vs IL2CPP

`Mono` and `IL2CPP` are techniques for compiling C# code to platforms (android, ios, webgl, macos, windows,...).

By default,

- `Mono` uses `JIT (just in time)` compiler to convert C# -> Assembly code.
- `IL2CPP` uses `AOT (ahead of time)` compiler to convert C# -> C++ code.


## Limitations

- At this time (2022-02-07), we cannot use any class in `System.Reflection.Emit` namespace.
And generic type only work for `reference type (string, object,...) and int type`,
and it does not work for `value` type.

Note: From Unity editor 2022.1 version, we can use `Full Generic Sharing` when choose IL2CPP.
But it will increase app size !


## References

- [Burst vs. IL2CPP: Generics](https://www.jacksondunstan.com/articles/5282)

- [IL2CPP Overview](https://docs.unity3d.com/Manual/IL2CPP.html)

- [Feature preview: IL2CPP Full Generic Sharing in Unity 2022.1 beta](https://blog.unity.com/technology/feature-preview-il2cpp-full-generic-sharing-in-unity-20221-beta)

- [IL2CPP Internals: Generic sharing implementation](https://blog.unity.com/technology/il2cpp-internals-generic-sharing-implementation)
