### <a name="signedxml-and-encryptedxml-breaking-changes"></a>Критические изменения в SignedXml и EncryptedXml

|   |   |
|---|---|
|Подробные сведения|Исправления системы безопасности в .NET Framework 4.6.2 для <xref:System.Security.Cryptography.Xml.SignedXml?displayProperty=name> и <xref:System.Security.Cryptography.Xml.EncryptedXml?displayProperty=name> привели к различиям в поведении во время выполнения. Например, примененная к объекту директива<ul><li>Если документ содержит несколько элементов с одинаковым атрибутом <code>id</code>, один из которых является целевым корнем подписи, такой документ будет считаться недействительным.</li><li>Теперь недействительными считаются документы, использующие неканонические алгоритмы преобразования XPath в ссылках.</li><li>Теперь недействительными считаются документы, использующие неканонические алгоритмы преобразования XSLT в ссылках.</li><li>Любая программа, использующая удаленные с внешнего ресурса подписи, не сможет сделать это.</li></ul>|
|Предложение|Разработчикам следует изучить, как используются <xref:System.Security.Cryptography.Xml.XmlDsigXsltTransform>, <xref:System.Security.Cryptography.Xml.XmlDsigXsltTransform> и производные от <xref:System.Security.Cryptography.Xml.Transform> типы, поскольку получатель документа не всегда сможет обработать его.|
|Область|Дополнительный номер|
|Версия|4.6.2|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.Security.Cryptography.Xml.Transform?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.Xml.XmlDsigXPathTransform?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.Xml.XmlDsigXsltTransform?displayProperty=nameWithType></li></ul>|

