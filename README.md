# metafile
A simple file format for describing heirarchical data. It's an alternative for xml-like file formats.

# Syntax
The format only defines two constructs i.e.
- nodes
- strings
Any other structure in the format is defined by the format's usage.

## Strings
- The format supports quoted strings and unquoted strings.
- There's three types of quotes that can be used, i.e. `\``, `"` and `'`.
- For quoted strings the quotation characters can be escaped with a back slash, otherwise any other escaping that's done is upto interpratation by the format's usage.
- Strings that contain any whitespace, `@` and / or any quotation marks should be quoted.
- Quoted strings can extend beyond multiple lines.
- Non quoted strings can contain any character other than the aformentioned quotation marks, whitespace or `@` which is reserved for tags.

## Nodes
- Nodes are used to represent the heirarchy.
- Each node contains a tag which is prefixed by the `@` symbol followed by an unquoted string
- Nodes can be nested inside curly braces.
- Attributes can be specified outside or inside the curly braces.
- The format supports specifying the attributes without keys.

## Example
```
@window title="Hello world" width=50% height=50% x=center y=center
{
  @vstack width=auto height=auto padding=10px border=10px x=center y=center
  {
    @h1 "Hello world"
    @sep height=2px
    @h4 "
    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum"
  }
}
```
## Anyways...
This repo just contains syntax highlighting for this format. I do not plan on publishing it to the marketplace since this format is just something I plan on using for code generation in c. But if you want to add support for syntax higlighting in this format, then just clone the repo and use the `Install extension from location...` feature to install it.