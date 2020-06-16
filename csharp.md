?

if aaa.B is null, then b is null

```
        [TestMethod]
        public void Test() 
        {
            var aaa = new AAA();
            var b = aaa.B?.Index;
        }

        public class AAA
        {
            public int Index { get; set; }

            public BBB B { get; set; }

            public class BBB
            {
                public int Index { get; set; }
            }
        }
```


Can I use Task.Delay as a timer?
https://stackoverflow.com/questions/42219885/can-i-use-task-delay-as-a-timer/42219948

use System.Reactive

```
IDisposable subscription =
    Observable
        .Interval(TimeSpan.FromSeconds(1.0))
        .Subscribe(x => execute());
```
