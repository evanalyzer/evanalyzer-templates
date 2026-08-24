# evanalyzer-templates

Project and pipeline templates for [evanalyzer](https://github.com/evanalyzer/evanalyzer): `.evapt` project templates under [project_templates/](project_templates/) and `.evapipe` pipeline templates under [pipeline_templates/](pipeline_templates/).

## Structure

Both top-level folders are split the same way:

```
project_templates/
  evanalyzer/
    <template-name>.evapt      # built-in templates, shipped with the app
  <contributed-folder>/
    <template-name>.evapt      # community-contributed template
    README.md                  # description, image provenance, porting/usage notes
    images/
      example1.tif             # example input/output images
      example2.tif

pipeline_templates/
  evanalyzer/
    <template-name>.evapipe    # built-in templates, shipped with the app
  <contributed-folder>/
    ...                        # same layout as above
```

**`evanalyzer/`** is special: whatever is placed there is packaged and published together with the application itself, so those files are flat — no per-template folder, README or images. Everything outside `evanalyzer/` is instead picked up for the downloads section on the evanalyzer website, and follows the one-folder-per-template layout above so each contribution is self-contained and easy to review, add, or remove independently.

Every `.evapt`/`.evapipe` file must still deserialize against evanalyzer's current `ProjectTemplate`/`PipelineTemplate` types — this is checked in CI (see [.github/workflows/check-templates.yml](.github/workflows/check-templates.yml)) against the schema in [evanalyzer/evanalyzer](https://github.com/evanalyzer/evanalyzer). A file's `meta` block already carries the template's name, description, tags, category and authors, so a contributed folder's `README.md` doesn't need to repeat that — use it for anything the file can't hold, like where the example images came from or notes on the underlying pipeline.


## License

See [LICENSE](LICENSE).
