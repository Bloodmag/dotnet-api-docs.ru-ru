### <a name="listboxitem-isselected-binding-issue-with-observablecollectionlttgtmove"></a>Проблема привязки ListBoxItem IsSelected ObservableCollection&lt;T&gt;. Перемещение

|   |   |
|---|---|
|Подробные сведения|Вызов <xref:System.Collections.ObjectModel.ObservableCollection%601.Move(System.Int32,System.Int32)> или <xref:System.Collections.ObjectModel.ObservableCollection%601.MoveItem(System.Int32,System.Int32)> с коллекцией, привязанный к <xref:System.Windows.Controls.ListBox?displayProperty=name> с выбранным элементов может привести к страницам с выделением будущих или unselection из <xref:System.Windows.Controls.ListBox?displayProperty=name> элементов.|
|Предложение|Вызов <xref:System.Collections.ObjectModel.Collection%601.Remove(%600)?displayProperty=name> и <xref:System.Collections.ObjectModel.Collection%601.Insert(System.Int32,%600)?displayProperty=name> вместо <xref:System.Collections.ObjectModel.ObservableCollection%601.Move(System.Int32,System.Int32)> будет решить эту проблему. Кроме того, эта проблема была устранена в .NET Framework 4.6 и может быть решена путем обновления до этой версии платформы .NET Framework.|
|Область|Дополнительный номер|
|Версия|4.5|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.Collections.ObjectModel.ObservableCollection%601.Move(System.Int32,System.Int32)?displayProperty=nameWithType></li><li><xref:System.Collections.ObjectModel.ObservableCollection%601.MoveItem(System.Int32,System.Int32)?displayProperty=nameWithType></li></ul>|

