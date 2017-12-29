# iOS (Operating System / Platform)

## Core Concepts


### Auto-layout
Links
* https://developer.apple.com/library/content/documentation/UserExperience/Conceptual/AutolayoutPG/index.html
* https://videos.raywenderlich.com/courses/81-rwdevcon-2017-vault-tutorials/lessons/2

##### Tips
* use Interface Builder on Xcode, because writing auto-layout code sucks.
* Constraints are relationships between 2 UI objects, represented by linear equations that must be satisfied.
* Avoid stringent "re-layout" logic, and leverage the cascading effect of constraint priorities to allow the constraints to resolve themselves.
