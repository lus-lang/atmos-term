# term

Measures and lays out text for a terminal: display width with wide characters and emoji, wrapping and truncating that keep colors, tables, boxes, spinners, and progress bars.

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

The package requires Lus 2.0. It needs no permissions. It calls no `pledge` of its own, so the program that loads it keeps control of its permissions.

The reference is in the doc comments of `term.lus`. Run `lus doc term.lus` to print it.
