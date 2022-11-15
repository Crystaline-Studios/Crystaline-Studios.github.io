## **Welcome to crystaline studios style guide**
This was created to keep the code clean, readable, simple, and intuitive.

## **Script Organization**
At the top of the file you should have 1-3 lines of comments explaining what the script does and is used for like a tldr for it.
Then you should get your big important frameworks like knit or matter or whatever im using at the time your reading this

example

``` lua
-- Requires knit and matter so uhhh...
local Knit = require(game:GetService("ReplicatedStorage").Packages.Knit)
local Matter = require(game:GetService("ReplicatedStorage").Packages.Matter)
```

Put a new tab if theres 2 or more things above.
After that you should get your replicatedstorages moderationservices and modules.
``` lua
-- Requires knit and matter and reparents
local Knit = require(game:GetService("ReplicatedStorage").Packages.Knit)
local Matter = require(game:GetService("ReplicatedStorage").Packages.Matter)

local ReplicatedStorage = game:GetService("ReplicatedStorage")
local ModerationService = Knit:GetService("ModerationService")
local Roact = require(game:GetService("ReplicatedStorage").Packages.Roact)
```

Try sorting them by size or alphabetical order whatever comes first to your head.
After you got all your services and modules move onto variables

for simplicity sakes heres how it should be fully organized.
Loader Modules
(tab if needed)
Services and modules this script is gonna use
(tab if needed)
Constants like an instance that the script is gonna keep on using the entire time and unchanging
variables that change
logic or OPP property creation
(tab)
logic or OPP Function creation


## **Variable Declaration?**
Where should you declare variables exactly?
Well you should declare them **Always** with local keyword and avoid shared and _G as these lead to bugs that are stupidly hard to find and fix avoid using global tables.
And **always** declare them with an name that explains itself

For example for bool values make it sound like a yes no question for example
```lua
local DoBanning = true
local IsAmazing = true
```

Avoid using odd names like V or C or A and try giving it a full name if possible.
and always name variables to the values name or other idenifiers. ex local ReplicatedStorage = game:GetService("ReplicatedStorage")