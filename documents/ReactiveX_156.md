# ReactiveX
*summery*
![](http://reactivex.io/assets/operators/legend.png =100%x)

By convention, in this document, calls to onNext are usually called “emissions” of items, whereas calls to onCompleted or onError are called “notifications.”

A “hot” Observable may begin emitting items as soon as it is created, and so any observer who later subscribes to that Observable may start observing the sequence somewhere in the middle. A “cold” Observable, on the other hand, waits until an observer subscribes to it before it begins to emit items, and so such an observer is guaranteed to see the whole sequence from the beginning.
