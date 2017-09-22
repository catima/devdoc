# Catalog dump

Currently, the only possibility to create a Catima catalog is by using the Web-based admin panel. A simple possibility to dump a catalog from Catima does not exist.

Some of the data can be accessed through the JSON API, but this is not intended for dumping the catalog.

Importing a complete catalog is also not possible. Only a basic implementation for importing data using CSV files exist.

As a result, we would need to have an option for dumping a catalog and for creating a catalog from a dump.

A dump typically contains the following information:

- the catalog structure
- the data
- the files associated with some of the fields
- all the pages and menus if defined

The catalog dump and load works as a task from the command line.

A catalog can be dumped using the command:

	rake catalog:dump catalog=<catalog-slug> dir=<dump-directory>

And for loading a catalog _(not yet implemented)_:

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

