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

### WorkshopWizard
The easiest way to get set up for the workshop is to use the [WorkshopWizard.jl](https://github.com/crstnbr/WorkshopWizard.jl). It will
* download the workshop materials,
* install and precompile all Julia package dependencies, and
* make the interactive IJulia/[Jupyter notebooks](http://jupyter.org) front-end globally available.

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
and use the web interface (your browser should pop up) to navigate to the workshop directory. That's it!

For [troubleshooting](https://crstnbr.github.io/WorkshopWizard.jl/dev/troubleshooting/#Troubleshooting-1) and [manual installation instructions](https://crstnbr.github.io/WorkshopWizard.jl/dev/troubleshooting/#Manual-installation-of-a-workshop-1) check out the WorkshopWizard [documentation](https://crstnbr.github.io/WorkshopWizard.jl/dev/).

## Poster

<a href="https://github.com/crstnbr/JuliaOulu20/raw/master/orga/poster.pdf"><img src="https://github.com/crstnbr/JuliaOulu20/raw/master/orga/poster.png" width=400px></a>
