# 自定义背景文件，android: shape的使用


```
<?xml version="1.0" encoding="utf-8"?>  
<selector xmlns:android="http://schemas.android.com/apk/res/android">  
    <item android:state_pressed="true" >  
        <shape xmlns:android="http://schemas.android.com/apk/res/android"  
            android:shape="rectangle">  
            <!-- 渐变 -->   
            <gradient    
                android:startColor="#55B4FE"    
                android:endColor="#3d8FFB"    
                android:angle="-90"  
                android:type="linear"/>    
            <!-- 描边 -->    
            <stroke android:width="1dip"  
                android:color="#d3d3d3"  
                />  
            <!-- 圆角 -->    
            <corners  
                android:topRightRadius="0dp"       
                android:bottomLeftRadius="10dp"     
                android:topLeftRadius="0dp"      
                android:bottomRightRadius="10dp"      
                />  
              
        </shape>  
          
          
    </item>  
    <item>  
        <shape xmlns:android="http://schemas.android.com/apk/res/android"  
            android:shape="rectangle">  
              
            <solid android:color="#ffffff" />            
            <!-- 描边 -->    
            <stroke android:width="1dip"  
                android:color="#d3d3d3"  
                />  
            <!-- 圆角 -->    
            <corners  
                android:topRightRadius="0dp"       
                android:bottomLeftRadius="10dp"     
                android:topLeftRadius="0dp"      
                android:bottomRightRadius="10dp"      
                />  
              
              
        </shape>  
    </item>  
</selector>  
```
#### **说明：**
##### gradient：渐变

android: startColor 渐变开始的颜色

android:endColor 渐变结束的颜色

android:centerColor 中间点的颜色

ndroid:angle是渐变角度，必须为45的整数倍。

android:type  linear线性渐变;radial径向渐变

android:gradientRadius 径向渐变的半径

##### solid：填充
android:color 使用的填充颜色

stroke：描边

android:width 描边的宽度，

android:color 描边的颜色。

我们还可以把描边弄成虚线的形式，设置方式为：

android:dashWidth="5dp" 一个'-'的宽度

android:dashGap="3dp" 间隔的宽度


##### corners：圆角
android:radius为角的弧度，值越大角越圆。

分开设置：

android:topRightRadius="20dp"    右上角  

android:bottomLeftRadius="20dp"    右下角  

android:topLeftRadius="1dp"    左上角  

android:bottomRightRadius="0dp"    左下角  

##### padding:内间隔