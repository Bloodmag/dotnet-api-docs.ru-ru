### <a name="missing-target-framework-moniker-results-in-40-behavior"></a>Отсутствие моникера целевой платформы приводит к поведению версии 4.0

|   |   |
|---|---|
|Подробные сведения|Приложения без атрибута <xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name>, примененного на уровне сборки, будут автоматически запускаться с использованием семантики (особенностей) платформы .NET Framework 4.0. Для обеспечения высокого качества рекомендуется явным образом применить ко всем двоичным файлам атрибут <xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name>, указывающий версию платформы .NET Framework, в которой они были созданы. Обратите внимание, что при использовании моникера целевой платформы в файле проекта MSBuild будет автоматически применять <xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name>.|
|Предложение|Атрибут <xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name> должен быть предоставлен либо путем его добавления непосредственно в сборку, либо путем указания целевой платформы в [файле проекта или с помощью графического интерфейса свойств проекта Visual Studio](http://blogs.msdn.com/b/visualstudio/archive/2010/05/19/visual-studio- managed-multi-targeting-part-1-concepts-target-framework-moniker-target-framework.aspx).|
|Область|Значительно|
|Версия|4.5|
|Тип|Среда выполнения|

