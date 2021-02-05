# er-diagram

My own custom package for drawing ER diagrams.

## Installation

Clone this repository to your `texmf/tex/latex` directory, then rename the directory containing this project from `tex-er-diagram` to `er-diagram`.

* With a standard install of LaTeX on macOS, the `texmf/tex/latex` directory should be in `~/Library/texmf/tex/latex`.

## Usage

To use, simply add `\usepackage{er-diagram}` to the document.

The package requires the use of the `tikzpicture` environment, and uses the `\pic` command.

### Entities

To draw an entity, use the `pic` command with an `entity` modifier.

```latex
  \pic [position] { entity = {{entityId}
      {entityTitle}
      {
        entityProperties
      }
  }};
  ```

Other entity variants include `entityweak` and `entityassociative`.

### Relationships

To draw relations, use a `draw` command with the degree modifiers.

```latex
  \draw[many-omany] (emp) -- node[label,above]{works for} (brew);
```

To specify the degree of the relationship, use a ``{degree}-{degree}`` modifier.

Degrees include:

* `one`
* `oone`
* `many`
* `omany`

## Examples

See [examples](./examples/basic.tex) for more examples.

