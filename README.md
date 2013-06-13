# A flat-file “port” of @bradfrost's Pattern Lab using Jekyll

## How it works

1. the index file has an include statement for each stratum of the design system (Atoms, Molecules, Organisms, Templates). Pages can live in actual Jekyll pages for now.
2. this included file is itself a list of include statements, bringing in every element of the appropriate type individually
3. higher order types, like molecules, consist of html and include statements that incorporate the lower orders (for example, an organism might include two molecules and three atoms)

This system is easy to maintain and create – the downside is that when a new Atom (for example) is created, _atoms.html_ (the file listing every Atom) must be manually updated. **This is because Jekyll does not allow for looping or iterating through *include* statements.**

Personally, I can live with that.
