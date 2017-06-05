# lightline\_tagbar

Vim plugin providing a function intended as a tab component for
[lightline.vim](https://github.com/itchyny/lightline.vim).

Wraps a call to the function provided by
[Tagbar](https://github.com/majutsushi/tagbar) that displays the tag inside
which the cursor is currently held.

## Usage

```vim
let g:lightline = {
\	'component_function': {
\		'tagbar': 'lightline_tagbar#component',
\	},
\	'active': {
\		'right': [
\			['lineinfo'],
\			['percent'],
\			['tagbar', 'fileformat', 'fileencoding', 'filetype'],
\		],
\	},
\}
```

## Configuration

```vim
" printf-compatible string that accepts a single value - the name of the tag.
let g:lightline_tagbar#format = '%s'

" Flags argument passed to tagbar#currenttag. See documentation of that
" function for details.
let g:lightline_tagbar#flags = ''
```
