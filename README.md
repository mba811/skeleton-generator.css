This repo shows how to automatically create a skeleton file (for styling textbooks).

# Running

- `npm install`
- `./node_modules/.bin/lessc style/precalc.less` generates the CSS file

For additional information see the [skeleton posts](http://philschatz.com/tags/#css) at [philschatz.com](http://philschatz.com).


# Directory Layout

- [./style/slots/](./style/slots/) contains abbreviated slot files to run the example
- [./style/skeleton/](./style/skeleton/) contains the bulk of the autogeneration code

# Conventions Used

- _private_ mixins (local to a file) are prefixed with a `x-`
- 2 spaces indent
- all mixins are namespaced
- variable parameters should be used sparingly (ie `.foo(@var) {...}`)
- parametric mixins are used only to create empty base slots (ie `.foo(...) { .. }`) or for the skeleton
- the `@return: ` _hack_ is only used to define book-specific `.kinds()` and internally in the skeleton
