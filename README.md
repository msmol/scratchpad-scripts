# Scratchpad Select

An easy way to bring back a specific window from SwayWM's scratchpad

## Usage

Add the following (or similar) to your sway config:

```
bindsym $mod+minus exec termite --name=launcher -e /path/to/scratchpad-select
for_window [app_id="^launcher$"] floating enable, border pixel 1, opacity 0.8
```

Hit `$mod+minus` to open prompt

- selecting a window and hitting "Enter" will bring that window out of the scratchpad in floating mode
- selecting a window and hitting "Alt+Enter" will bring that window out of the scratchpad in tiled mode

## Limitations

- If you have no windows in your scratchpad, you will still see termite pop up for a fraction of a second before closing
- Alt+Enter for tiled mode will first bring the window back in floating mode, and then immediately toggle it to be tiled. I haven't figured out how to do both steps at once.

## Contributing

Any and all contributions welcome!
