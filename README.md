# Copy paste guide for RxJava1-to-RxJava2

```Observable``` is ```Flowable```

```CompositeSubscription``` is ```CompositeDisposable```

```Subscription``` is ```Disposable```

```Observable.subscribe(Observer)``` is ```Observable.subscribeWith(DisposableSubscriber)``` (if you want it to return a disposable)

```Observable.Transformer<T,T>``` is ```FlowableTransformer<T,T>```

```Action1``` is ```Consumer```
```Action2``` is ```BiConsumer```
```Action0``` is ```Action```

```Actions.empty()``` is ```Functions.EMPTY_ACTION```

Similarly there are ```Functions.emptyConsumer``` and ```Functions.emptyBiconsumer```

```TestSubscription.getNextEvents()```  is  ```TestSubscription.values```
