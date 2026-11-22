# term

`term` measures and lays out text for a terminal. It computes the display width of text that holds wide characters and emoji, wraps and truncates text without losing its colors, and draws tables, boxes, spinners, and progress bars.

The following example lays out the output of a tool that copies files.

```lus nocheck
local term = require("https://atmosp.here/2.0/term.lus")

print(term.width("\u{65e5}\u{672c}\u{8a9e}"))          --> 6
print(term.wrap(text, 72))
print(term.table({ { "name", "size" }, { "lus", "2.1 MB" } }, { header = true }))

local bar = term.progress({ total = #files, label = "Copying" })
for _, file in ipairs(files) do
    copy(file)
    bar:tick()
end
```

The package requires Lus 2.0 and declares no permissions. It never calls `pledge`, so the program that loads it keeps control of its permissions.

The reference is in the doc comments of `term.lus`, which `lus doc term.lus` prints.
