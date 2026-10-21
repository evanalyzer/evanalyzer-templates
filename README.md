# evanalyzer-templates

Project templates and modules for [evanalyzer](https://github.com/evanalyzer/evanalyzer): `.evatemplate` project templates under [project_templates/](project_templates/) and `.evamodule` modules under [module_templates/](module_templates/).

## Structure

Both top-level folders are split the same way:

```
project_templates/
  evanalyzer/
    <template-name>.evatemplate  # built-in templates, shipped with the app
  <contributed-folder>/
    <template-name>.evatemplate  # community-contributed template
    README.md                    # description, image provenance, porting/usage notes
    images/
      example1.tif               # example input/output images
      example2.tif

module_templates/
  evanalyzer/
    <template-name>.evamodule    # built-in modules, shipped with the app
  <contributed-folder>/
    ...                          # same layout as above
```

**`evanalyzer/`** is special: whatever is placed there is packaged and published together with the application itself, so those files are flat — no per-template folder, README or images. Everything outside `evanalyzer/` is instead picked up for the downloads section on the evanalyzer website, and follows the one-folder-per-template layout above so each contribution is self-contained and easy to review, add, or remove independently.

Every `.evatemplate`/`.evamodule` file must still deserialize against evanalyzer's current `ProjectTemplate`/`ModuleTemplate` types — this is checked in CI (see [.github/workflows/check-templates.yml](.github/workflows/check-templates.yml)) against the schema in [evanalyzer/evanalyzer](https://github.com/evanalyzer/evanalyzer). A file's `meta` block already carries the template's name, description, tags, category, authors and version, so a contributed folder's `README.md` doesn't need to repeat that — use it for anything the file can't hold, like where the example images came from or notes on the underlying pipeline.


## License

See [LICENSE](LICENSE).
