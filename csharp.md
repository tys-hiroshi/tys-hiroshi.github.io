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

### Linq

#### for文でSQLを発行するのではなく、Whereに条件を不定数付けてSQLを実行する場合

https://tech.blog.aerie.jp/entry/2015/09/25/103325

```
// 検索条件を動的に生成する
var orExList = new List<Expression<Func<Hoge, bool>>>();
CreateExpression(ref orExList, targetList)
var target = _db.Set<Hoge>()
    .Where(ExpressionCombiner.OrElse(orExList))
    .Select(a => a);
```

```
internal static void CreateExpression(ref List<Expression<Func<Hoge, bool>>> orTargetExpression, string[] targetList)
{
    foreach(string targetItem in targetList)
    {
        orTargetExpression.Add(x => x.TargetItem == targetItem);
    }
}
```
