### <a name="wpf-dispatchersynchronizationcontextcreatecopy-now-returns-a-new-copy-instead-of-the-current-instance"></a>Метод DispatcherSynchronizationContext.CreateCopy WPF теперь возвращает новую копию вместо текущего экземпляра

|   |   |
|---|---|
|Подробные сведения|В .NET Framework 4 метод <xref:System.Windows.Threading.DispatcherSynchronizationContext.CreateCopy> возвращал ссылку на текущий экземпляр главным образом в качестве оптимизации производительности. В .NET Framework 4.5 он возвращает новый экземпляр, что позволяет впервые делать заключение о том, что одинаковые ссылки указывают на то, что выполняющийся поток находится в правильном контексте синхронизации.  Маловероятно, что будет затронут код, который проверяет подлинность этих ссылок, но в связи с изменением необходимо протестировать код, который вызывает <xref:System.Windows.Threading.DispatcherSynchronizationContext.CreateCopy>, в ходе миграции на .NET Framework 4.5 или более позднюю версию.|
|Предложение|Учитывайте, что <xref:System.Windows.Threading.DispatcherSynchronizationContext.CreateCopy> теперь возвращает новый объект <xref:System.Threading.SynchronizationContext?displayProperty=name>. Ранее код, который использовал эквивалентность ссылок, на самом деле не проверялся на нахождение в правильном контексте, но проверяется при создании в .NET 4.5 или более поздних версиях.  Хотя маловероятно, что это приведет к серьезным проблемам, проверки путей к затронутому коду должно быть достаточно для определения проблемы.|
|Область|Дополнительный номер|
|Версия|4.5|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.Windows.Threading.DispatcherSynchronizationContext.CreateCopy?displayProperty=nameWithType></li></ul>|

