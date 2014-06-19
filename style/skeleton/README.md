                              )       \   /      (
                             /|\      )\_/(     /|\
    *                       / | \    (/\|/\)   / | \                      *
    |'.____________________/__|__o____\'|'/___o__|__\___________________.'|
    |                           '^'    \|/   '^'                          |
    |                                   V                                 |
    |           HERE BE DRAGONS!!!                                        |
    |                                                                     |
    | ._________________________________________________________________. |
    |'               l    /\ /     \\            \ /\   l                '|
    *                l  /   V       ))            V   \ l                 *
                     l/            //                  \l
                                   V

Everything in this directory should **NOT** change for different books so it can be considered "magic".


If you **do* need to change something in here it would probably be to:

1. Increase the maximum context length
2. Add a new `type` of content or `part` (ie exercise, note, figure)

# Skeleton Code

This code will "build" the skeleton and generate all permutations of `@contexts` for the slots.
The interesting bits are each content `@type`.

There is a `.selector()` that defines the **selector** to match a CNXML element (`@type`)

- for `c:note` or `c:example` it would be a `[data-type="foo"]`
- for `c:list` it would be a `ul, ol, [data-type="list"]`
- for `c:figure` it would be a `figure`

There is a `.template()` that defines all the _slots_ **inside** a CNXML element

- for `c:note` it would be a `.style()`, `.title()`.  and `.body()`
- for `c:exercise` it would be a `.style()`, `.title()`
- for `c:figure` it would be a `.style()`, `.title()` and `.caption()`

There are at least 2 files in here:

- `content-templates.less` defines all the content types and which slots they have
- `generator.less` actually generates all the skeleton selectors
