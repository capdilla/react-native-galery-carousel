# react-native-galery-carousel
Galery carousel for react native



## Demo

![react-native-galery-carousel](https://media.giphy.com/media/3oKIPuWr6Mp7bOtYVG/giphy.gif)
![react-native-galery-carousel](https://media.giphy.com/media/3oKIPj1guAZsLVqQfK/giphy.gif)


## Usage

```
$ npm install --save react-native-galery-carousel
```

```javascript
const imagesDemo = [
    {
        path: '/UYiroysl.jpg'
    },
    {  
        path: '/UPrs1EWl.jpg'
    },
    {    
        path: '/MABUbpDl.jpg'
    },
    {    
        path: '/KZsmUi2l.jpg'
    },
    {    
        path: '/2nCt3Sbl.jpg'
    },
    {    
        path: '/lceHsT6l.jpg'
    }
];
import GaleryCarousel from 'react-native-galery-carousel';

    render () {
      <View>
        <GaleryCarousel
          dataImage={imagesDemo}
          joinFirst={'http://i.imgur.com'}
          defaultImageIndex={2}
          onLongPress={(key,element)=>{console.log(key,element)}}
          mainImageComponents={
            <View style={{flex:1,backgroundColor:"transparent"}}>
              <Text style={{color:"#fff"}}>Hello</Text>
            </View>
          }
        />
      </View>
    }
```

## Props

Prop | Description | Type | Default
------ | ------ | ------ | ------
**dataImage** | the array of the image to show in the carousel | array | `[]`
**getImageFrom** | the key of the array where you wanna get the image | string | `"path"`
**joinFirst** | if you wanna join a link before **example** https://my-host-name.com/ `path` | string | `""`
**joinLast** | if you wanna join string after **example** `path`/key="1255665" | string | `""`
**defaultImageIndex** | index of the first image to show | Number | `1`
**mainImageComponents** | if you wanna render a component in the Main image | Component | `<View/>`
**mainHeight** | size of the galery carousel | Number | `280`
**onLongPress** | each item of the carousel | function | `function`


## TODO
- [x] Implement 'onLongPress' in the scrollView images
