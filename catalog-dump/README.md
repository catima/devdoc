# Catalog dump

Currently, the only possibility to create a Catima catalog is the web-based sys-admin dashboard.

Catalogs can be dumped using the "Export" feature available in the administration panel of each catalog. Catalogs can be exported in multiple formats, but the "Catima" format is the only one you can import in another Catima instance.

Dumping a catalog in cli can be done using the command:

	rake catalog:dump catalog=<catalog-slug> dir=<dump-directory>

A dump typically contains the following information:

- the catalog structure
- the data
- the files associated with some of the fields
- all the pages and menus if defined

And for importing a catalog _(currently in beta)_:

	rake catalog:load dir=<dump-directory>

The folder [example-dumps](example-dumps) contains some examples of catalog dumps that can be used to try it out, and for testing.


## Dump directory structure

A dump directory must contain at least:

- a file called __`meta.json`__ containing informations related to the dump itself.
- a directory __`structure`__ with at least a file called __`catalog.json`__.


## The meta file

The __meta.json__ file contains the creation date of the catalog dump and the dump format version (JSON-formatted):

```json
{
  "dump_created_at": "2000-01-01 00:00:01 UTC",
  "dump_version": "1.0"
}
```

