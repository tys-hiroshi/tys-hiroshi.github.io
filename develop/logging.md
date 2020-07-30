https://logging.apache.org/log4net/release/manual/configuration.html#attributes

環境([envname])ごとにApp.configやWeb.configが変更できる前提で、log4net.config.xml を環境ごとに別にしたいとき

Properties/AssemblyInfo.cs

```
[assembly: log4net.Config.XmlConfigurator(Watch=false)]
```

app.[envname].config/web.[envname].config

```
<appSettings>
  <add key="log4net.Config" value="log4net.config.[envname].xml"/>
  <add key="log4net.Config.Watch" value="True"/>
</appSettings>
```

