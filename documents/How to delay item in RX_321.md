# How to delay item in RX
---
author: Jason Song <metaseed@gmail.com>
version: 1.0.0
tag: []
enable: [toc]
---

## Delay in same interval
```csharp
#r "nuget:System.Reactive.Linq/4.4.1"
using System;
using System.Reactive.Linq;

new int[] {1,4,3}
.ToObservable()
.Zip(Observable.Interval(TimeSpan.FromMilliseconds(1000)),(a,b)=>a)
.Concat(Observable.Never<int>())
.Subscribe(a=>Console.WriteLine(a));

while (true) {Thread.Sleep(100);}
```
## Delay in configed interval
```csharp
#r "nuget:System.Reactive.Linq/4.4.1"
using System;
using System.Reactive.Linq;

var items = new[]{('a', 0), ('b', 1000), ('c', 2000)}
.ToObservable()
.Delay(t =>Observable.Timer(TimeSpan.FromMilliseconds(t.Item2)))
.Select(t => t.Item1)
.Subscribe(i => Console.WriteLine(i));

while (true) {Thread.Sleep(100);}
```