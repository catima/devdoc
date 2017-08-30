# Catalog dump

Currently, the only possibility to create a Catima catalog is by using the Web-based admin panel. A simple possibility to dump a catalog from Catima does not exist.

Some of the data can be accessed through the JSON API, but this is not intended for dumping the catalog.

Importing a complete catalog is also not possible. Only a basic implementation for importing data using CSV files exist.

As a result, we would need to have an option for dumping a catalog and for creating a catalog from a dump.

A dump typically contains the following information:

- the catalog structure
- the data
- the files associated with some of the fields

The dump is contained in its own directory with a precise structure:

	-- catalog-dump
	  |-- structure.json
	  |-- data
	    |-- item-type-1.json
	    |-- item-type-2.json
	    |-- ...
	  |-- files
	    |-- item-type-X
	      |-- field-Y
	        |-- file-1.pdf
	        |-- file-2.md
	        |-- file-3.docx
	        |-- ...
	  |-- catalog
	  	 |-- ...

The catalog dump and load works as a task from the command line.
