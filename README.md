# Cascadingss

A grid system made with scss modules.

## Technologies
* sass
* css modules

## Getting Started
### setup sass:
vite
```
npm add -D sass
```
create react app
```
npm install sass
```
### setup structure:
```
src
├── styles
│   ├── global.scss          # put your global styles here
│   ├── layout.module.scss   # copy desktop or mobile layout content here
│   ├── theme.module.scss    # add your theme variables here
│   ├── shared.module.scss   # add your shared styles here
```

## Usage:
add global styles to the app:
```
├── src
│   ├── App.js

import './styles/global.scss';
```

styling component:
```
// styles have all component custom styles
// layout have all page shape styles

import styles from './myComponent.module.scss';
import layout from '../../styles/layout.module.scss';

const MyComponent = function () {
  return (
    <div className={`${layout['flex']} ${layout['justify-center']}`}>
      <div className={`${layout['col-3']}`}>
        <h1 className={`${styles['styled-header']}`}>box 1</h1>
      </div>
      <div className={`${layout['col-3']}`}>
        <h1 className={`${styles['styled-header']}`}>box 2</h1>
      </div>
      <div className={`${layout['col-3']}`}>
        <h1 className={`${styles['styled-header']}`}>box 3</h1>
      </div>
    </div>
  );
};

export {MyComponent};
```

## Classes List:
| class | properties |
|-------|------------|
| w | 1/12~12/12 | width: 8.333333%~100%;|
| w | screen | width: 100vw;|
| h | 1/12~12/12 | height: 8.333333%~100%;|
| h | screen | height: 100vh;|
| block | display: block;|
| inline-block | display: inline-block;|
| inline | display: inline;|
| flex | display: flex;|
| inline-flex | display: inline-flex;|
| table | display: table;|
| inline-table | display: inline-table;|
| table-caption | display: table-caption;|
| table-cell | display: table-cell;|
| table-column | display: table-column;|
| table-column-group | display: table-column-group;|
| table-header-group | display: table-header-group;|
| table-row-group | display: table-row-group;|
| table-row | display: table-row;|
| flow-root | display: flow-root;|
| grid | display: grid;|
| inline-grid | display: inline-grid;|
| contents | display: contents;|
| list-item | display: list-item;|
| hidden | display: none;|
| visible | visibility: visible;|
| invisible | visibility: hidden;|
| flex-row | flex-direction: row;|
| flex-row-reverse | flex-direction: row-reverse;|
| flex-col | flex-direction: column;|
| flex-col-reverse | flex-direction: column-reverse;|
| flex-wrap | flex-wrap: wrap;|
| flex-wrap-reverse | flex-wrap: wrap-reverse;|
| flex-nowrap | flex-wrap: nowrap;|
| flex-1  | flex: 1 1 0%;|
| flex-auto | flex: 1 1 auto;|
| flex-initial | flex: 0 1 auto;|
| flex-none | flex: none;|
| grow | flex-grow: 1;|
| grow-0 | flex-grow: 0;|
| shrink | flex-shrink: 1;|
| shrink-0 | flex-shrink: 0;|
| order-1~12 | order: 1~12;|
| order-first | order: -9999;|
| order-last | order: 9999;|
| order-none | order: 0;|
| justify-start | justify-content: flex-start;|
| justify-end | justify-content: flex-end;|
| justify-center | justify-content: center;|
| justify-between | justify-content: space-between;|
| justify-around | justify-content: space-around;|
| justify-evenly | justify-content: space-evenly;|
| content-center | align-content: center;|
| content-start | align-content: flex-start;|
| content-end | align-content: flex-end;|
| content-between | align-content: space-between;|
| content-around | align-content: space-around;|
| content-evenly | align-content: space-evenly;|
| items-start | align-items: flex-start;|
| items-end | align-items: flex-end;|
| items-center | align-items: center;|
| items-baseline | align-items: baseline;|
| items-stretch | align-items: stretch;|
| self-auto | align-self: auto;|
| self-start | align-self: flex-start;|
| self-end | align-self: flex-end;|
| self-center | align-self: center;|
| self-stretch | align-self: stretch;|
| self-baseline | align-self: baseline;|
| pt-1~6 | $spacing-1~6;|
| pr-1~6 | $spacing-1~6;|
| pb-1~6 | $spacing-1~6;|
| pl-1~6 | $spacing-1~6;|
| mt-1~6 | $spacing-1~6;|
| mr-1~6 | $spacing-1~6;|
| mb-1~6 | $spacing-1~6;|
| ml-1~6 | $spacing-1~6;|

### responsive:
| layout | class | breakpoint |
|------|------|-------|
desktop first | -xl, -lg, -md, -sm, -xs| 1280px, 1024px, 768px, 640px, 576px|
mobile first | -sm, -md, -lg, -xl, -2xl| 640px, 768px, 1024px, 1280px, 1536px|
