## Kantan Tracker Usage

### Plots
Use the NewPlot button on the main toolbar to create a new live plot instance. Each live plot instance has its own associated configuration defining what values are to be plotted and various other display related settings. At any one time, a live plot instance can be attached to a single PIE world, or the editor world. The world it is attached to will determine what actors are available when specifying properties to plot.

By default, world attachment is automatic, meaning the plot will attach to the main PIE instance, or the editor world if no PIE instance is running. The only time it should be necessary to manually specify the attached world is when debugging multiplayer PIE.

Any time a PIE session is terminated, attached live plot instances will automatically send their accumulated plot data to a stored plot window. The live plot instance will maintain its configuration settings, so if a new PIE session is started, it will automatically begin plotting the same properties again.

### Plot Toolbar
In the top right of each plot instance is a toolbar containing a few toggle options, along with a dropdown for selecting the attached world.

### Plot Types
In the bottom left of a live plot instance is a button which cycles through various methods of specifying values to plot.
- Single object, multiple properties.
The plot will have a single target (usually an actor, but can be any object reachable from an actor). Each series on the plot is a property specified relative to the target.
- Multiple object, single property.
Each series in the plot represents an independent actor/object. A single property is specified to be plotted for each target. Only properties common to all specified targets will be available.
- Data repository.
Rather than using property bindings, each series is a value in the Kantan Tracker data repository. This is a repository of transient values which need to be updated from within a Blueprint or C++ code, generally from within a tick function.

### Command Bar
The command bar, at the bottom of a plot instance, is a context-sensitive input control from which most configuration of plots can be done using keyboard entry alone. Options are given in a dropdown list, which will display when typing but can also be invoked by pressing the 'Down' arrow key.

### Plot Status
The status display lists current configuration details, and provides feedback icons for any inconsistencies between configuration and world state.

### Plot
The plot itself displays a series legend and automatic axis scaling and labelling. It is possible to manually adjust axis ranges via the command bar, and the visual appearance of the plot can be controlled from the plugin settings.

[Index]({{ site.baseurl }}{% link index.md %})
