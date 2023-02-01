Ionic
页面构成https://ionicframework.com/docs/layout/structure
基本结构
<ion-app>
  <ion-header>
    <ion-toolbar>
      <ion-title>Header</ion-title>
    </ion-toolbar>
  </ion-header>

  <ion-content class="ion-padding">
    <h1>Main Content</h1>
  </ion-content>

  <ion-footer>
    <ion-toolbar>
      <ion-title>Footer</ion-title>
    </ion-toolbar>
  </ion-footer>
</ion-app>

栅格系统 基本为12等分，offset为偏移量，如果布局整体超过12会换行，调整大小size

<ion-app>
  <ion-header>
    <ion-toolbar>
      <ion-title>微信</ion-title>
    </ion-toolbar>
    </ion-header>
  <ion-content>
    <ion-grid>
      <ion-row>
        <ion-col class="tab1" size="2">返回</ion-col>
        <ion-col class="tab1" offset="8" size="2">退出</ion-col>
      </ion-row>
    </ion-grid>
    
    <ion-grid>
      <ion-row>
        <ion-col offset="3" size="4">1</ion-col>
        <ion-col>2</ion-col>
        <ion-col>3</ion-col>
        <ion-col>4</ion-col>
        <ion-col>5</ion-col>
        <ion-col>6</ion-col>
      </ion-row>
    </ion-grid>
    
    <ion-grid>
      <ion-row>
        <ion-col>1</ion-col>
        <ion-col>2</ion-col>
        <ion-col>3</ion-col>
        <ion-col>4</ion-col>
        <ion-col>5</ion-col>
        <ion-col>6</ion-col>
        <ion-col>7</ion-col>
        <ion-col>8</ion-col>
        <ion-col>9</ion-col>
        <ion-col>10</ion-col>
        <ion-col>11</ion-col>
        <ion-col>12</ion-col>
      </ion-row>
    </ion-grid>
  </ion-content>
</ion-app>


绝对定位可以使标签位置和组件实际位置不同，来实现不同屏幕宽度下排列位置依然相同。例如：由于屏幕宽度不同导致，未按预想位置排列，右图应为源代码排列位置，左图为绝对定位排列实际效果
    ![1 jpg](https://user-images.githubusercontent.com/50564769/216077821-8e6bd1e0-90ca-443e-898b-59b74e4fb84b.png)
![image](https://user-images.githubusercontent.com/50564769/216077891-774c700a-3024-4d0b-afbe-160f1a4b39cb.png)


当position属性值设置为absolute时，则开启了元素的绝对定位
绝对定位：
1.开启绝对定位，会使元素脱离文档流
2.开启绝对定位以后，如果不设置偏移量，则元素的位置不会发生变化
3.绝对定位是相对于离他最近的开启了定位的祖先元素进行定位的（一般情况，开启了子元素的绝对定位都会同时开启父元素的相对定位）
    如果所有的祖先元素都没有开启定位，则会相对于浏览器窗口进行定位
4.绝对定位会使元素提升一个层级
5.绝对定位会改变元素的性质，
内联元素变成块元素，display:block
    块元素的宽度和高度默认都被内容撑开

position: absolute;

/*left: 100px;
top: 100px;*/


底层用绝对定位实现：push向右移动布局 pull向左拉动布局
<ion-row>
        <ion-col size="4" push="2"><div style="border:1px solid #f00; padding:5px 0">4/12</div></ion-col>
        <ion-col size="8" pull="1"><div style="border:1px solid #00f">8/12</div></ion-col>
      </ion-row>

app.component2.html


9中主题色
https://ionicframework.com/docs/theming/colors

<ion-button>Default</ion-button>
<ion-button color="primary">Primary</ion-button>
<ion-button color="secondary">Secondary</ion-button>
<ion-button color="tertiary">Tertiary</ion-button>
<ion-button color="success">Success</ion-button>
<ion-button color="warning">Warning</ion-button>
<ion-button color="danger">Danger</ion-button>
<ion-button color="light">Light</ion-button>
<ion-button color="medium">Medium</ion-button>
<ion-button color="dark">Dark</ion-button>




常用组件https://ionicframework.com/docs/components




Badge 徽章
https://ionicframework.com/docs/api/badge
 


Icon 图标 

https://ionicframework.com/docs/api/icon
 





