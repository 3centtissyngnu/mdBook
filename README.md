# mdBook

Personal implementation of Gitbook in Rust

**This is still a work in progress...**

## Contributions

Contributions are highly apreciated. Here are some ideas:

- **Create new renderers**, at the moment I have only created a renderer that uses handlebars, pulldown-cmark and renders to html. But you could create a renderer that uses another template engine, markdown parser or even outputs to another format like pdf.
- **Add tests** I have not much experience in writing tests, all help to write meaningful tests is thus very welcome
- **Smaller tasks** I try to add a lot of the remaining tasks on the issue tracker with the label: `Enhancement`. Just pick one that looks interesting. The majority of the tasks are small enough to be tackled by people who are unfamiliar with the project.

If you have an idea for improvement, create a new issue. Or a pull request if you can :)

## cli tool

#### init

If you run `mdbook init` in a directory, it will create a couple of folders and files you can start with.
This is the strucutre it creates at the moment:
```
book-test/
├── book
└── src
    ├── chapter_1.md
    └── SUMMARY.md
```
`book` and `src` are both directories. `src` contains the markdown files that will be used to render the ouput to the `book` directory.

You can also pass a directory to `mdbook init` to use instead of the current directory:
```
mdbook init path/to/my/book
```

<sup>**Not implemented yet:** using `--theme` flag will create a theme folder with the default theme in `src` so that you can customize it.</sup>

#### build

Use `mdbook build` in the directory to render the book. You can also give a path as argument to use instead of the current directory.


## lib

Aside the command-line tool, this crate can also be used as a library. 

-------------------------------------------------------

For more information about what is left on my to-do list, check the issue tracker

## License

All the code is released under the ***Mozilla Public License v2.0***, for more information take a look at the [LICENSE](LICENSE) file