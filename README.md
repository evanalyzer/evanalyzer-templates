# evanalyzer-templates

Community-contributed templates for [evanalyzer](https://github.com/evanalyzer-project). A template packages an `.evapt` file together with example images so others can see what it does and reuse it.

## Structure

Each template lives in its own folder under `templates/`:

```
templates/
  <template-name>/
    <template-name>.evapt   # the evanalyzer project template file
    README.md               # description, image provenance, porting/usage notes
    images/
      example1.tif          # example input/output images
      example2.tif
```

One folder per template keeps each contribution self-contained and easy to review, add, or remove independently.

A `.evapt` file must validate against [schema.json](schema.json) (the `ProjectTemplate` schema: `meta`, `classification`, `plate`, and `pipelines`). Its `meta` block already carries the template's name, description, tags, category and authors, so the folder's `README.md` doesn't need to repeat that — use it for anything the file can't hold, like where the example images came from or notes on the underlying pipeline.


## License

See [LICENSE](LICENSE).
