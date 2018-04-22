### <a name="gridviews-with-allowcustompaging-set-to-true-may-fire-the-pageindexchanging-event-when-leaving-the-final-page-of-the-view"></a>Если в GridViews для свойства AllowCustomPaging установлено значение true, может возникать событие PageIndexChanging при выходе из последней страницы представления

|   |   |
|---|---|
|Подробные сведения|В результате ошибки в .NET Framework 4.5 иногда событие <xref:System.Web.UI.WebControls.GridView.PageIndexChanging?displayProperty=name> не срабатывает для <xref:System.Web.UI.WebControls.GridView?displayProperty=name> со свойством <xref:System.Web.UI.WebControls.GridView.AllowCustomPaging?displayProperty=name>.|
|Предложение|Эта проблема была устранена в .NET Framework 4.6 и может быть решена путем обновления до этой версии платформы .NET Framework. Чтобы обойти эту проблему, приложение может иметь явный BindGrid в любом <code>Page_Load</code>, которое вызывает эти условия (<xref:System.Web.UI.WebControls.GridView?displayProperty=name> находится на последней странице, а Last<xref:System.Web.UI.WebControls.GridView.PageSize?displayProperty=name> отличается от <xref:System.Web.UI.WebControls.GridView.PageSize?displayProperty=name>). Кроме того, приложение можно изменить, чтобы разрешить разбивку на страницы (вместо пользовательского разбиения по страницам), поскольку в этом случае проблемы не возникают.|
|Область|Дополнительный номер|
|Версия|4.5|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.Web.UI.WebControls.GridView.AllowCustomPaging?displayProperty=nameWithType></li></ul>|

