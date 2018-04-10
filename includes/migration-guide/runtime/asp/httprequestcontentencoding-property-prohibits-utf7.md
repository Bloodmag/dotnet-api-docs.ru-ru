### <a name="httprequestcontentencoding-property-prohibits-utf7"></a>HttpRequest.ContentEncoding property prohibits UTF7

|   |   |
|---|---|
|Подробные сведения|Начиная с .NET Framework 4.5, кодировка UTF-7 запрещена в <xref:System.Web.HttpRequest?displayProperty=name>s' тела. Данные для приложений, которые зависят от поступающих данных UTF-7, в некоторых случаях декодируются неверно.|
|Предложение|В идеальном случае приложения должны быть обновлены для использования в кодировку UTF-7 не <xref:System.Web.HttpRequest?displayProperty=name>s. Кроме того, устаревшее поведение можно восстановить с помощью атрибута <code>aspnet:AllowUtf7RequestContentEncoding</code> элемента [appSettings](https://msdn.microsoft.com/library/hh975440(v=vs.110).aspx).|
|Область|Пограничный случай|
|Версия|4.5|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.Web.HttpRequest.ContentEncoding?displayProperty=nameWithType></li></ul>|

