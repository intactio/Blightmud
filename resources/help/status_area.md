# Status area methods

These methods allow you to control the height and content in the status area.

##

***blight.status_height([height]) -> int***
Set or get the status area height. The first and last row will always be
rendered as bars. But you can still print to these bars. Setting the height to
0 will hide the status area.

- `height`  The height to set (0 <= height <= 5) *Optional*
- Returns the current status area height

***blight.status_line(index, line)***
Prints a line to the status area. If you print to a 'bar line' the content will be integrated into the bar. The "(more)" info shown when scrolling will always
be allowed to occupy space before your custom line when applicable.

- `index`   The line to print to (0 based), if it's greater then the height of your area it will always default to last line. If it's less than 0 it will default to 0.
- `line`    The line you want to print

***blight.bar_color([color])***
Sets the color of the bars: the first and last status area lines, the top rows
and the tab indicator. Text printed on a bar without its own color uses this
color too.

- `color`   A 256-color index (`240`), a hex color (`"#585858"`) or a name
            (`"black"`, `"red"`, `"green"`, `"yellow"`, `"blue"`, `"magenta"`,
            `"cyan"`, `"white"`, `"bright_red"` ... `"bright_white"`, `"grey"`).
            `nil` or `"default"` restores the default green. *Optional*
