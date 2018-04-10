### <a name="etw-eventlisteners-do-not-capture-events-from-providers-with-explicit-keywords-like-the-tpl-provider"></a>EventListeners трассировки событий Windows не выполняется сбор событий из поставщиков с явной ключевые слова (например, поставщик библиотека параллельных задач)

|   |   |
|---|---|
|Подробные сведения|EventListeners трассировки событий Windows с пустой маской ключевого слова неправильно записывают события от поставщиков с явными ключевыми словами. В платформе .NET Framework 4.5 поставщик TPL начал предоставлять явные ключевые слова и привел к возникновению этой проблемы. В .NET Framework 4.6 EventListeners были обновлены, чтобы больше не вызывать эту проблему.|
|Предложение|Чтобы обойти эту проблему, замените вызовы <xref:System.Diagnostics.Tracing.EventListener.EnableEvents(System.Diagnostics.Tracing.EventSource,System.Diagnostics.Tracing.EventLevel)> с вызовами EnableEvents перегрузку, которая явно задает &quot;всех ключевых слов&quot; маски для использования: <code>EnableEvents(eventSource, level, unchecked((EventKeywords)0xFFFFffffFFFFffff))</code>. Кроме того эта проблема была устранена в платформе .NET Framework 4.6 и можно обращаться путем обновления для этой версии платформы .NET Framework.|
|Область|Пограничный случай|
|Версия|4.5|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.Diagnostics.Tracing.EventListener.EnableEvents(System.Diagnostics.Tracing.EventSource,System.Diagnostics.Tracing.EventLevel)?displayProperty=nameWithType></li></ul>|

