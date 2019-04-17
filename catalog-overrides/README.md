# Catalog-specific overrides

In CATIMA it is possible to override the catalog views, locales, assets and controllers. CATIMA looks for directories in its optional `catalogs` directory with as name the slug of a valid catalog.

**Assets** stored in `catalogs/:catalog_slug/assets`, in one of the directories `images`, `stylesheets` and `javascripts` are automatically added to the Rails application. For each catalog, the following assets are precompiled and can be used in the catalog views:

- `stylesheets/#{:catalog_slug}.css`
- `javascripts/#{:catalog_slug}.js`
- all non-JS/CSS in the catalog assets directory


**Locales** stored in `catalogs/:catalog_slug/locales/*.yml` are loaded automatically by Rails.

**Controllers** stored in `catalogs/:catalog_slug/controllers/:catalog_slug_*_controller.rb`. The following controllers can be overridden:

- catalogs -> `:catalog_slug_catalogs_controller.rb`
- simple_searches -> `:catalog_slug_simple_searches_controller.rb`
- advanced_searches -> `:catalog_slug_advanced_searches_controller.rb`
- items -> `:catalog_slug_items_controller.rb`
- pages -> `:catalog_slug_pages_controller.rb`

Examples can be found in the [catima/catalogs](https://github.com/catima/catalogs) repository.