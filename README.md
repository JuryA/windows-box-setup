# Windows Box Setup

This is an example repository to showcase how [Chocolatey][choco] and
[Boxstarter][box] can be used to bootstrap a Windows machine using a single
`box.zip` artifact. This method relies on the public [Chocolatey][choco] feed,
but can be adapted to any set of custom feeds.

## Development

Install [Chocolatey][choco] and [Boxstarter][box]:

```powershell
. { iwr -useb https://boxstarter.org/bootstrapper.ps1 } | iex; get-boxstarter -Force
```

The `artifacts\box.zip` file can be built by running `build.ps1`.

## Bootstrap a Computer

The packages `my.box.setup` and `my.box.setup.explorer` contain example
instructions to bootstrap a .NET developer environment. `my.vs2017.cake`
highlights how to install a Visual Studio extension using Chocolatey.

- Copy `box.zip` to a network share or to your target computer.
- Extract the archive and run either `install-mybox.ps1` or `install-mybox.bat`.
  This command will start a local copy of Boxstarter which will install the
  `my.box.setup` package.

## License

The license for this repository is explained in `LICENSE.txt`. Boxstarter's
license can be found [here][box_license].

[choco]: https://chocolatey.org/
[box]: https://boxstarter.org/
[box_license]: https://github.com/chocolatey/boxstarter/blob/master/LICENSE.txt
