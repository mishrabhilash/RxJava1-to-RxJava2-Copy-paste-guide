# Copy paste guide for RxJava1-to-RxJava2

Feel free to add more copy-paste guides

| Copy (RxJava1) | Paste (RxJava2) |Remarks|
| ------------- | ------------- | ------------|
|```Observable``` |```Flowable```|
|```CompositeSubscription```|```CompositeDisposable```|
|```Subscription```|```Disposable```|
|```Observable.subscribe(Observer)```|```Observable.subscribeWith(DisposableSubscriber)```|Only if you want it to return a disposable|
|```Observable.Transformer<T,T>```|```FlowableTransformer<T,T>```|
|```Action1```|```Consumer```| 
|```Action2```|```BiConsumer```|
|```Action0```|```Action```|
|```Func1<T,R>```|```Function<T,R>```| 
|```Func2<T1, T2, R>```|```BiFunction<T1, T2, R>```|
|```Func1.call(T)```|```Function.apply(T)```|
|```Actions.empty()```|```Functions.EMPTY_ACTION```|Similarly there are ```Functions.emptyConsumer``` and ```Functions.emptyBiconsumer```|
|```TestSubscription.getNextEvents()```|```TestSubscription.values```|
|```RxJavaCallAdapterFactory```|```RxJava2CallAdapterFactory```|
|```PublishSubject.asObservable()```|```PublishSubject.hide()```|
