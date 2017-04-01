# &#60;dsc-polymer-datatable&#62;

[![Build Status](https://travis-ci.org/discovery-tecnologia/dsc-polymer-datatable.svg?branch=master)](http://travis-ci.org/#!/discovery-tecnologia/dsc-polymer-datatable)
![Bower version](https://img.shields.io/bower/v/dsc-polymer-datatable.svg)
![](https://img.shields.io/pypi/l/Django.svg)

A material design implementation of a data table. Easy API integration.

Differential:

 * Easy to use
 * Cutumizable header buttons
 * Customizable style
 * API integration

## Demo

```
$ git clone https://github.com/discovery-tecnologia/dsc-polymer-datatable.git
$ cd dsc-polymer-datatable
$ npm install
$ npm install -g polymer-cli
$ polymer serve
```
Open browser: http://localhost:8080/components/dsc-polymer-datatable/demo/

## Usage

Install with:

```
$ bower i dsc-polymer-datatable --save
```

Example usage:

```html
<dsc-polymer-datatable
    id="my-component"
    selectable
    title="Albums"
    on-change="_handlerChange"
    on-select="_handlerSelect">
  <dsc-columns>
    <dsc-column type="number" label="ID" name="_id" hidden></dsc-column>
    <dsc-column type="string" label="Title" name="title" sortable></dsc-column>
    <dsc-column type="string" label="Category" name="category"></dsc-column>
    <dsc-column type="string" label="Created at" name="createdAt" sortable></dsc-column>
  </dsc-columns>
</dsc-polymer-datatable>
```

## API Reference

### Properties

| Property       | Description                                                      | Default |
|:---------------|------------------------------------------------------------------|---------|
| limit          | Quantity per page.                                               | null    |
| orderBy        | Current field of the document by which records are to be sorted. | null    |
| orderDirection | Sense of ordination. Ascending or descending. 'asc' or 'desc'.   | null    |
| pages          | Total number of pages.                                           | null    |
| page           | Current page number.                                             | null    |
| total          | Total items in all pages                                         | null    |

### Methods

| Method           | Description                                      |
|:-----------------|--------------------------------------------------|
| **setData**()    | Set array of objects by exitent items.           |

### Events

| Event            | Description                                      |
|:-----------------|--------------------------------------------------|
| datatable-change | Event of one or more of the following states: orderBy, orderDirection, page, limit. |
| datatable-select | On table selection change. Return all selecteds items data.                         |

## Test

Check sintax and execute selenium tests.

```
$ npm test
```

## TODO

 * internationalization
