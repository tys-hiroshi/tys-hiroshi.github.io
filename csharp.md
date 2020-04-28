?

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
