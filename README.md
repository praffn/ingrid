# 👵 ingrid
### A featherweight Sass grid library

Ingrid is derived from [Neat by Thoughbot](https://github.com/thoughtbot/neat), cut to the absolute minimum.

## Usage

### Getting started
Copy `ingrid.scss` to some place where you can import it in your Sass files.

```
@import "ingrid";
```

### Variables

* `$ingrid-gutter`<br>
  default: 1rem<br>
  Overwrite this to set the gutter between each column.

* `$ingrid-visual-color`<br>
  default: rgba(255, 0, 0, 0.1)
  Overwrite this to set the color of the columns in the auxilliary visual grid.

### Container

A container will just clear the column floats. Ingrid will not set max-width, padding or center your divs. That's up to you 💁‍.

```
@include ingrid-container;
```

### Column
Ingrid grids are always composed of 12 columns. You can set a column to take up 1-12 columns:

```
@include ingrid-column(<columns>);
```
Where `<columns>` is the number of columns.

### Push
You can push a column by n columns like this:
```
@include ingrid-push(<columns>);
```
Where `<columns>` is the number of columns to push

### Visual grid
To aid development you can create a visual grid on the container:
```
@include ingrid-visual;
```

------------
A huge thanks to Thoughtbot for Neat (and all their other wonderful tools). The reason for this little library arose when I had to work on a project that used a super old version of RubySass, where I tried to cut down compilation time. (I really miss LibSass)