# Catalog-specific overrides

In CATIMA it is possible to override the catalog views, locales, assets etc. CATIMA looks for directories in its optional `catalogs` directory with as name the slug of a valid catalog.

**Assets** stored in `catalogs/:catalog_slug/assets`, in one of the directories `images`, `stylesheets` and `javascripts` are automatically added to the Rails application. For each catalog, the following assets are precompiled and can be used in the catalog views:

- `stylesheets/#{:catalog_slug}.css`
- `javascripts/#{:catalog_slug}.js`
- all non-JS/CSS in the catalog assets directory



