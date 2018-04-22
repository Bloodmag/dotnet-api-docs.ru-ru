### <a name="remove-ssl3-from-the-wcf-transportdefaults"></a>Удаление Ssl3 из WCF TransportDefaults

|   |   |
|---|---|
|Подробные сведения|При использовании NetTcp для обеспечения безопасности транспорта и применении типа учетных данных сертификата протокол SSL 3 больше не является протоколом по умолчанию для согласования безопасного соединения. В большинстве случаев существующие приложения не должны затрагиваться, так как протокол TLS 1.0 всегда входил в список протоколов для NetTcp. Все существующие клиенты должны иметь возможность согласовывать подключение с помощью TLS версии не ниже 1.0.|
|Предложение|Если требуется Ssl3, воспользуйтесь одним из указанных ниже механизмов конфигурации и добавьте Ssl3 в список установленных протоколов.<ul><li><xref:System.ServiceModel.Channels.SslStreamSecurityBindingElement.SslProtocols></li><li><xref:System.ServiceModel.TcpTransportSecurity.SslProtocols></li><li>[<](~/docs/framework/configure-apps/file-schema/wcf/transport-of-nettcpbinding.md)</li><li>[Раздел &lt;sslStreamSecurity&gt; &lt;customBinding&gt;]~/docs/framework/configure-apps/file-schema/wcf/sslstreamsecurity.md)</li></ul>|
|Область|Пограничный случай|
|Версия|4.6.2|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.ServiceModel.Channels.SslStreamSecurityBindingElement.SslProtocols?displayProperty=nameWithType></li><li><xref:System.ServiceModel.TcpTransportSecurity.SslProtocols?displayProperty=nameWithType></li></ul>|

