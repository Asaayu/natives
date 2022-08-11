---
ns: MISC
---
## GET_FRAME_COUNT

```c
// 0xFC8202EFC642E6F2 0xB477A015
int GET_FRAME_COUNT();
```

Gets the number of the current frame being displayed.

## Return value
The number of the current frame being displayed.

## Examples
```lua
-- Create a thread
Citizen.CreateThread(function()
    -- Loop forever
    while true do
        -- Get the current number of frames that have been rendered
        local startCount = GetFrameCount()

        -- Wait one second
        Wait(1000)

        -- Get the number of frames that have been rendered since the last time we checked
        local endCount = GetFrameCount()

        -- Calculate the number of frames that have been rendered between the start and end counts
        local frameCount = endCount - startCount

        -- Print the output to the console, mentioning that it is an approximate value
        print("Approximate FPS: "..frameCount)
    end
end)
```
