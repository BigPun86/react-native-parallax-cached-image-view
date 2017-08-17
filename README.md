# react-native-parallax-cached-image-view

Parallax view with a cachable header image and header content.
This Module is an small improvement to react-native-parallax-view with some small fixes. Forther on it is able to cache images by using the react-native-img-cache. 

## Installation

```bash
$ npm i react-native-parallax-cached-image-view --save
```

## Demo

![parallax view demo](https://app.hyfy.io/v/abxui89EwKU/)

## Example

```jsx
<ParallaxView
    windowHeight={300}
    header={<Header author={author} />}
    blur={this.state.modalVisible ? 'light' : null}
    backgroundSource={{ uri: 'http://lorempixel.com/400/200/' }}
    scrollableViewStyle={{ backgroundColor: 'red' }}>
   <ParallaxBody/>
</ParallaxView>
```


## API (props)

| Prop | Required | Default  | Type | Description |
| :------------ |:---:|:---------------:| :---------------:| :-----|
| backgroundSource | YES | `null` | `object` | the `source` prop that get's passed to the background `<Image>` component. If left blank, no background is rendered |
| backgroundStyle | NO | `empty` | `object` | the `style` prop that get's passed to the background `<Image>` component. 
| header | NO | `null` | `renderable` | any content you want to render on top of the image. This content's opacity get's animated down as the scrollview scrolls up. (optional) |
| windowHeight | NO | `300` | `number` | the resting height of the header image. If 0 is passed in, the background is not rendered. |
| scrollableViewStyle | NO | `null` | `object` | this style will be mixed (overriding existing fields) with scrollable view style (view which is scrolled over the background) |
| ... | NO | | `...ScrollViewProps` | `{...this.props}` is applied on the internal `ScrollView` (excluding the `style` prop which is passed on to the outer container) |

