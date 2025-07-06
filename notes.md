# Goal
The goal is to be able to execute arbitrary commands by scrolling on the task bar.

# Outline
There are 3 parts to this doing this

## Detect scroll events
This is already present, just needs to be adapted
There is a setting "Scrolling on a task does" with options nothing/cycle through all tasks/windows.

## Adjust settings
The dropdown for what to do on scroll needs another entry "Execute Command".
When that is selected 2 text input boxes should appear (on for each scroll up / down command).

## Excute commands
This is already being done in the "plasma-applet-commandoutput" plasmoid.
In its qml it does something like  

PlasmoidItem {
    Plasma5Support.DataSource {
		id: executable
		engine: "executable"
        // ...
    }
    // ...
}

cfg_interval

# Potential issues
- Scrolling should be detected on the whole plasmoid, not just when scrolling over an entry in the bar
-  
