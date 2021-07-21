Personal copy of [`boyswan/vscode-glsl-literal`](https://github.com/boyswan/vscode-glsl-literal) with additional bugfix from [`aoitaku`](https://github.com/aoitaku/vscode-glsl-literal)

This patches support for the `/* glsl */` prefix.

Original README:

# vscode-glsl-literal

Adds GLSL syntax highlighting for JavaScript template literals.

## Match on

```js
glsl`` | glslify`` | frag`` | vert``;
```

## Example

```js
const vert = glsl`
  attribute vec4 aVertexPosition;
  uniform mat4 uModelViewMatrix;
  uniform mat4 uProjectionMatrix;
  void main() {
    gl_Position = uProjectionMatrix * uModelViewMatrix * aVertexPosition;
  }
`;
```

## Caveat

If you're not using glslify or another glsl processing library, you will need an identity function named as above to match the syntax.

```js
const glsl = (x) => x;
```
