## CSS grid layout

`css grid layout` 适用于web端的二维布局，能使项目以行列布局。它可以用于实现复杂的布局。

### 容器属性
+ `grid-template-columns`

+ `grid-template-rows`

+ `grid-template-areas`

+ `grid-template`

+ `grid-auto-rows`

+ `grid-auto-flow`

+ `grid-row-start`

+ `grid-column-start`

+ `grid`

+ `grid-gap`

+ `grid-row-grap`

+ `grid-column-grap`

### 1.1 `grid-template`
`grid-template`是一个缩写属性以定义 grid 的行列和区域(grid columns,rows and areas)

使用者可以用`grid-template-columns`,`grid-template-rows`,`grid-template-areas` 长属性设值。

``` css
/* 将对应的三个长属性设值为none，表示不再是明确的栅格，不再是栅格区，Rows和columns将暗中生成，它们的大小将通过grid-auto-rows和grid-auto-columns属性确定*/
grid-template :none; 

/* grid-template-rows / grid-template-columns values */
/* grid-template-areas grid-template-rows / grid-template-column values */

/* Global values */
grid-template: inherit;
grid-template: initial;
grid-template: unset;
```

### 1.2 `grid-template-columns`
定义了线网格列的名字和跟踪分级功能
```css
/* 默认值 表示不再是明确的栅格,columns将暗中生成,它们的大小将通过grid-auto-columns属性确定*/
grid-template-columns: none;

/* 长度 */
grid-template-columns: 100px 1fr;
grid-template-columns: [linename] 100px;
grid-template-columns: [linename1] 100px [linename2 linename3];
grid-template-columns: minmax(100px, 1fr); /* 定义了一个尺寸范围[min,max],若min>max 时，忽略max，即值为min */
grid-template-columns: fit-content(40%);
grid-template-columns: repeat(3, 200px);


/* <auto-track-list> values */
grid-template-columns: 200px repeat(auto-fill, 100px) 300px;
grid-template-columns: minmax(100px, max-content) repeat(auto-fill, 200px) 20%;
grid-template-columns: [linename1] 100px [linename2] repeat(auto-fit, [linename3 linename4] 300px) 100px;
grid-template-columns: [linename1 linename2] 100px repeat(auto-fit, [linename1] 300px) [linename3];
```
### 1.3 `grid-template-rows`
定义了线网格行的名字和跟踪分级功能(类似`grid-template-columns`)

### 1.4 `grid-template-areas`
`grid-template-areas`值为`grid areas`的值

```css
/* Keyword value */
grid-template-areas: none;

/* <string> values */ 
grid-template-areas: "a b"; /* 对应的grid-areas名*/
grid-template-areas: "a b b"
                     "a c d";
```

### 1.5 `grid-auto-rows`
用于指定隐藏创建的网络的行轨道大小

如果一个网格项目定位在行中，但不是用`grid-template-rows`明确定义大小，则默认创建网格轨道去hold it.

```css
/* Keyword values */
grid-auto-rows: min-content;
grid-auto-rows: max-content;
grid-auto-rows: auto;

/* <length> values */
grid-auto-rows: 100px;
grid-auto-rows: 20cm;
grid-auto-rows: 50vmax;

/* <percentage> values */
grid-auto-rows: 10%;
grid-auto-rows: 33.3%;

/* <flex> values */
grid-auto-rows: 0.5fr;
grid-auto-rows: 3fr;

/* minmax() values */
grid-auto-rows: minmax(100px, auto);
grid-auto-rows: minmax(max-content, 2fr);
grid-auto-rows: minmax(20%, 80vmax);

/* multiple track-size values */
grid-auto-rows: min-content max-content auto;
grid-auto-rows: 100px 150px 390px;
grid-auto-rows: 10% 33.3%;
grid-auto-rows: 0.5fr 3fr 1fr;
​​​​​​​grid-auto-rows: minmax(100px, auto) minmax(max-content, 2fr) minmax(20%, 80vmax);
grid-auto-rows: 100px minmax(100px, auto) 10% 0.5fr fit-content(400px);


```

### 项目属性
+ `grid-column`

+ `grid-column-end`

+ `grid-row`

+ `grid-row-end`



