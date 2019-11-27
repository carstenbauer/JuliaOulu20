# JuliaOulu20

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/crstnbr/JuliaOulu20/master)

An intermediate Julia workshop for undergraduate/graduate physicists which will take place in February 2020 at the [University of Oulu](https://www.oulu.fi/university/), Finnland. Only elementary Julia knowledge should be required to follow along.

Coursework: Equals to 2 ETCS points and contains the workshop lectures as well as a small contribution to the Julia ecosystem.

Registration: **If you're a student or employee at the University of Oulu** you can use the [registration form](http://tinyurl.com/juliaoulu20) to sign up for the workshop. The maximal number of participants is 50 and registrations are handled on a first-come first served basis.

Teacher: [Carsten Bauer](http://github.com/crstnbr), [University of Cologne](https://www.portal.uni-koeln.de/index.php?id=9441&L=1)

In case of questions, feel free to [contact me](http://github.com/crstnbr).

## Try it out live! (Beta)

Click on the [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/crstnbr/JuliaOulu20/master) badge to dive right into the workshop materials.

## Getting started

We will use Julia version 1.3 in the course. Go to the [julialang.org](https://julialang.org/downloads/) and install the binaries for your operating system.

### Automatic installation: WorkshopWizard.jl
The easiest way to get set up for the workshop is to use the [WorkshopWizard.jl](https://github.com/crstnbr/WorkshopWizard.jl). It will
* download the workshop materials,
* install and precompile all Julia package dependencies, and
* install the interactive IJulia/[Jupyter notebooks](http://jupyter.org) front-end (if necessary).

Fire up Julia and run the following command to install the WorkshopWizard.jl.
```julia
using Pkg; pkg"add https:/github.com/crstnbr/WorkshopWizard.jl"
```

Afterwards, you can load the package and run the wizard (this may take a while).
```julia
using WorkshopWizard
WorkshopWizard.run_wizard()
```

By default, the wizard will download the workshop materials to your Desktop (on windows) or your home directory (on linux/macOS).

After the installation has completed you're good to go. Start the notebook server with
```julia
using IJulia
notebook()
```
and navigate to the workshop directory. That's it!

If, for some reason, the wizard doesn't work for you, turn to the manual instructions below.


### Manual installation

#### Workshop Materials

If you have `git` installed, just `git clone https://github.com/crstnbr/JuliaOulu20`. If you don't have `git` installed, or can't access it from the commmand line, start a fresh Julia instance and run
```julia
using LibGit2
LibGit2.clone("https://github.com/crstnbr/JuliaOulu20", "some/where/on/my/computer/JuliaOulu20")
```
where you replace `some/where/on/my/computer/` with a download path to your liking.

#### Installion and Precompilation of Package Dependencies

Open up a Julia REPL and navigate to the `JuliaOulu20` directory
```julia
cd("some/where/on/my/computer/JuliaOulu20")
```
We now install all Julia package dependencies (*instantiate* the workshop's Julia environment) and precompile them by running the following snippet
```julia
using Pkg
pkg"activate ."
pkg"instantiate"
pkg"precompile" # this may take a while
pkg"activate"
```

#### IJulia/Jupyter

In this (a bit outdated) [youtube video](https://www.youtube.com/watch?v=4Rnm0n39DCs) I show how to install Julia + IJulia/Jupyter on windows. Basically it should be as easy as (in a fresh Julia REPL)
```julia
using Pkg
Pkg.add("IJulia")
```
If you have a local python installation and IJulia doesn't recognize it, you may give it a hint with
```julia
ENV["PYTHON"] = "path/to/my/python-executable"
Pkg.build("IJulia")
```

You now that things are set up correctly when you can start the notebook server

```julia
using IJulia
notebook()
```

## Poster

<a href="https://github.com/crstnbr/JuliaOulu20/raw/master/orga/poster.pdf"><img src="https://github.com/crstnbr/JuliaOulu20/raw/master/orga/poster.png" width=400px></a>
