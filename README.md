# An art direction image component for use with Gatsby

At the moment, Gatsby Image only supports one image. This is a modified version of [Gatsby Image](https://www.gatsbyjs.org/packages/gatsby-image/) to use when art direction images are needed (display a different image at a certain breakpoint). Supports two images, either fixed or fluid, with a customizable breakpoint.

## Requirements and Usage

[Gatsby Plugin Styled Components](https://www.gatsbyjs.org/packages/gatsby-plugin-styled-components/) is required.

Add the ArtImg component to your src/components/ directory and import it where needed.

Uses all the same [Gatsby Image props](https://www.gatsbyjs.org/packages/gatsby-image/#gatsby-image-props), with the exception of replacing `fixed` and `fluid` with the desired mix of the props below.

New props:

* fluidMobile - Object
* fluidDesktop - Object
* fixedMobile - Object
* fixedDesktop - Object
* breakPoint (Optional) - Number - default is 768

Two images (mobile and dekstop) are required. For images where art direction isn't needed, use the standard Gatsby Image component.

## Example

```js
<ArtImg
  fluidMobile={data.someImage.childImageSharp.fluid}
  fluidDesktop={data.someImage.childImageSharp.fluid}
  breakPoint={980}
  alt={`Doggo being a good boy waiting for treats`}
  fadeIn={false}
  background={true}
  critical
/>
```