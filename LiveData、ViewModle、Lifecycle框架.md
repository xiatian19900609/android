# LiveData、ViewModle、Lifecycle框架
> #### LiveData 是一个可以感知 Activity 、Fragment生命周期的数据容器，当 LiveData 所持有的数据改变时，它会通知相应的界面代码进行更新。同时，LiveData 持有界面代码 Lifecycle 的引用，这意味着它会在界面代码（LifecycleOwner）的生命周期处于 started 或 resumed 时作出相应更新，而在 LifecycleOwner 被销毁时停止更新。（优点：不用手动控制生命周期，不用担心内存泄露，数据变化时会收到通知。）

```
//定义方式(kotlin)
var name = MutableLiveData<String>()
//可以通过postValue更新数据
name.postValue("..")
```
> #### ViewModel是用来管理UI相关的数据的，同时ViewModel还可以用来负责UI组件间的通信。

```
//定义ViewModle
class MainViewHodle : ViewModel() {
    val name = MutableLiveData<String>()
    /**
     * 异步请求获取数据
     */
    fun loadData() {
        name.postValue("sss")
    }
}

```
> #### MainViewHodle中提供了相应的方法。在MainActivity中只需要在回调里面触发方法即可。这里面的liveData使用是MutableLiveData即可变的LiveData，因为每次请求数据之后我们需要重新设置liveData里面的值。这样的话在对应的MainActivity中只需要监听LiveData做好界面显示逻辑就可以了。

```
class MainActivity : AppCompatActivity() {
    lateinit var viewHodle: MainViewHodle
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)
        viewHodle = ViewModelProviders.of(this).get(MainViewHodle::class.java)
        val observer = Observer<String> { s ->
            tv.text = s
        }
        viewHodle.name.observe(this, observer)
        
         viewHodle.loadData()
    }
}
```


