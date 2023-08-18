# AppleScripts

Here's are some Apple Scripts I created. Freel free to use at your own risks, or suggest any improvements as I'm not expert.

- [Fake Typing](#fake-typing)

## Fake Typing

Useful when you want to create a demo video, and ensure there's no typo.

```applescript
set command to "ls -lsa"

tell application "iTerm" to activate # Remove or change

delay 2 # So you can move the mouse away or anything else

repeat with i from 1 to count of characters in command
	set letter to character i of command
	tell application "System Events" to keystroke letter
	delay (random number from 0.025 to 0.075)
end repeat

tell application "System Events" to keystroke return
```

[Compiled version](scripts/fake-typing.scpt).
