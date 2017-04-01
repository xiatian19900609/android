## 函数的参数使用约定的参数示例

##### 自定义一个常量类
```
public class TypeDefine {
    public static final String JC_ZQ = "1"; //竞彩足球
    public static final String JC_LQ = "2";    //竞彩篮球
    public static final String ZC_SPF1 = "3";//	传足14场

    /**
     * 彩种定义
     */
    @Retention(RetentionPolicy.SOURCE)
    @StringDef({JC_ZQ, JC_LQ, ZC_SPF1})
    public @interface  LotteryType{}
}

```
##### 函数的参数引用这个自定义常量
```
    public void loadOrderList(final Context context , @TypeDefine.LotteryType String lotteType) {
    
    }
```
