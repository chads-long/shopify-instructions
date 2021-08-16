# Shopify only has limited amount of data that it can store about a product, and next-to-no data that it can store about a collection. However, you can add hundreds of tags to a single product. 

## First, we should devise a permanent method for tagging items. There are a few reasons why:

### Most vitally, this would add the ability to have data *(from a file that's saved centrally)* display as a section on every product's page that you want to specify, based on any criteria that is tagged.
With this method, you'd only have to edit one file to update every product of a specific line/material/shape/etc. if something were to change with that product line. This is the only method I've seen through Shopify that would make this possible. Shopify generates pages by calling up files and using those as sections based on certain conditions. For instance, on this [collections page](https://store.columns.com/collections/all), there are at least 8 of these files:
- The header
- The footer
- The navigation menus
- The description (at the time of writing, it's the 8 tiles that show product categories) 
- The filter menu
- The collection page itself
- Each product *(those reuse one file to generate every product on the page)*
- Each product preview that appears after clicking on a product.

As an example, assuming every product were properly tagged, making a new Octagonal column for example, and tagging it `shape_octagonal`, the product's page could automatically populate with information about octagonal columns such as the plan shapes or dimensions of the different sizes of octagonal columns we offer.

### It should clearly differentiate architectural orders between **_parts of a product_** and **_overall products_**

- **Problem example**: When attempting to create a collection, if you choose *"tag equal to"* and choose *"Ionic"*, and add a *"Product Type"* field, then make that field *"Columns"*, you'll now have a new collection with Corinthian and other orders included as well since the `ionic` tag will be present if there's an Attic base or the shaft has Ionic dimensions. Fixing this would also make Collection creation easy, since we'd only need 1 *"tag equal to"* field as opposed to using many filters to narrow the new collection.
- **Solution** Use a prefix such as `baseorder_`, `base-order_`, or `caporder_` on **sets** where it's applicable (including when a product has no base, such as a Greek Doric: `base-order_none`) but *NOT* use those prefixes for a **stand-alone product**, such as a single Capital. 
For that, we could simply do `archorder_`, `arch-order`, `overall-order_`, or `prod-order_`. _(It'd be better to have the prefixes spelled out as much as possible since it makes the meaning of the tag obvious to the person working on it. For instance, it'd take very little time for a new salesperson or developer to understand what each tag means.)_

### Clearly differentiate materials and Architectural Orders

- **Problem example**: The `composite` tag is attributed to products that are manufactured with a _composite material_ as well as products that belong in the _Composite Order of Architecture_. There's no way to easily solve this problem without manually modifying the products in those collections. In this case, it'd be helpful to have prefixed tags differentiate based on many criteria. In this instance, this situation would be easily avoided with `material_composite` and `arch-order_composite`.

### Differentiate materials per part in a set if needed. (I'm not 100% sure this is something that would happen, but for instance a Wood column with a cast resin capital, or FRP shaft with a PolyStone cap.)

 - `cap-material_wood`
 - `shaft-mat_polystone`
 - `base-mat_frp`

---
# Current tags
## These can be 

### abacus_

- _round
- _square
- _octagonal\*
- _custom\*

### base-material_

- _cast-marble
- _fiberglass
- _imp
- _polyurethane
- _polystone
- _wood\*

### base_

- _attic
- _doric
- _ionic
- _roman-doric
- _tuscan
- _custom\*

### era_\*

- _greek
- _modern
- _renaissance
- _roman

### capital-material_

- _cast-marble
- _fiberglass
- _imp
- _polyurethane
- _polystone
- _wood\*
- _frp\*
- _polystone\*

### capital_

- _angular-ionic
- _composite
- _corinthian
- _doric
- _empire
- _erechtheum
- _greek-angular-ionic
- _greek-corinthian
- _greek-doric
- _greek-erechtheum
- _ionic
- _modern-composite
- _roman-corinthian\*
- _roman-doric
- _roman-ionic
- _scamozzi
- _tuscan
- _tower-of-winds\* **(greek)**
- _temple-of-winds\* **(greek)**
- _tower-of-the-winds\* **(greek)**
- _tower-of-the-winds\* **(greek)**
- _mutulary-doric\* **(roman)**
- _denticulated-doric\* **(roman)**

### column-type_

- _art-deco
- _belley
- _contemporary
- _mirror-image

### complete_

- _cap-only
- _false
- _true

### custom_

- _arlington

### exclude_

- _ionic

### shaft-material_\*

- _acv
- _advanced-cellular-vinyl
- _architectural-wood
- _classic-stone
- _fiberglass
- _frp
- _maple **(add _species-wood to listing with this tag)**
- _polylite
- _polystone
- _pvc
- _species-wood
- _stain-grade
- _wood
- _\_fiberglass\*_ **(added from material_)**
- _\_frp\*_ **(added from material_)**
- _\_polylite\*_ **(added from material_)**

### necking_

- _false
- _ornate
- _true

### plan-type_

- _octagonal
- _round
- _square

### plinth_shape

- _round
- _square

### product-line_\*

- _polybox
- _polystone\*
- _turncraft\* **(can't remember if caps/bases only or if columns are included)**
- _classic-stone
- _pergola-columns
- _premium-architectural-polystone

### ~~shaft-material_~~ **(make material_ into shaft-material, move these to it)**
- ~~_fiberglass~~
- ~~_frp~~
- ~~_polylite~~


### shaft-surface_

- _fluted
- _panel
- _paneled
- _plain
- _raised-panel
- _recessed-panel
- _recessed-panel-double
- _recessed-panel-single
- _recessed-panel-triple
- _rope
- _rope-twist
- _\_reeded_ **(added from shaft_)**
- _\_cabled_ **(added from shaft_)**


### shaft-taper_

- _non
- _none
- _non-tapered
- _tapered
- _continuous
- _entasis
- _one-third-two-third
- _hyperbolic-curve

### ~~shaft_~~

- ~~_belley~~ **(-> column-type_)**
- ~~_reeded~~ **(-> shaft-surface_)**
- ~~_cabled~~ **(-> shaft-surface_)**
- ~~_non~~ **(-> taper_)**
- ~~_non-tapered~~ **(-> taper_)**

### shape_

- _octagonal
- _round
- _square

### warehouse_

- _12
- _18
- _19
- _2
- _22
- _23
- _5
- _7
