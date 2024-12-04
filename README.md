custom
======

Add custom code to the `init.zsh` file.

Custom functions can go in the `functions` subdirectory, where the name of the
file is the name of the function. These functions will be lazy loaded.

For example, this function:
```zsh
foo() {
  print bar
}
```

will become a lazy loaded function if created as a file named `foo` in the
`functions` subdirectory, containing:
```zsh
print bar
```

There is a special kind of function that can also be added to the `functions`
subdirectory: completion definitions that will be loaded by `compinit`. These
must have file names starting with `_`.

Having an `init.zsh` file or functions inside the `functions` subdirectory are
both optional. You can have one, the other, or both.
