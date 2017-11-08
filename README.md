# Copy paste guide for RxJava1-to-RxJava2

Feel free to add more copy-paste guides

```Observable``` is ```Flowable```  

```CompositeSubscription``` is ```CompositeDisposable```  

```Subscription``` is ```Disposable```  

```Observable.subscribe(Observer)``` is ```Observable.subscribeWith(DisposableSubscriber)``` (if you want it to return a disposable)  

```Observable.Transformer<T,T>``` is ```FlowableTransformer<T,T>```  

```Action1``` is ```Consumer```  
```Action2``` is ```BiConsumer```  
```Action0``` is ```Action```  

```Func1<T,R>``` is ```Function<T,R>```  
```Func2<T1, T2, R>``` is ```BiFunction<T1, T2, R>```  
```Func1.call(T)``` is ```Function.apply(T)```  

```Actions.empty()``` is ```Functions.EMPTY_ACTION```  

Similarly there are ```Functions.emptyConsumer``` and ```Functions.emptyBiconsumer```  

```TestSubscription.getNextEvents()```  is  ```TestSubscription.values```

```RxJavaCallAdapterFactory``` is ```RxJava2CallAdapterFactory```
