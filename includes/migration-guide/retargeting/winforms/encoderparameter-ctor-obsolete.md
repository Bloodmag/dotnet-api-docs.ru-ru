### <a name="encoderparameter-ctor-is-obsolete"></a>EncoderParameter ctor устарел

|   |   |
|---|---|
|Подробные сведения|Конструктор <xref:System.Drawing.Imaging.EncoderParameter.%23ctor(System.Drawing.Imaging.Encoder,System.Int32,System.Int32,System.Int32,System.Int32)> устарел. При его использовании будут выводиться предупреждения сборки.|
|Предложение|Несмотря на то что <xref:System.Drawing.Imaging.EncoderParameter.%23ctor(System.Drawing.Imaging.Encoder,System.Int32,System.Int32,System.Int32,System.Int32)>конструктор будет продолжать работать, следующий конструктор следует использовать во избежание сборке устаревшие предупреждение при повторной компиляции кода с помощью средств .NET 4.5: <xref:System.Drawing.Imaging.EncoderParameter.%23ctor(System.Drawing.Imaging.Encoder,System.Int32,System.Drawing.Imaging.EncoderParameterValueType,System.IntPtr)>.|
|Область|Дополнительный номер|
|Версия|4.5|
|Тип|Изменение целевой платформы|
|Затронутые API|<ul><li><xref:System.Drawing.Imaging.EncoderParameter.%23ctor(System.Drawing.Imaging.Encoder,System.Int32,System.Int32,System.Int32,System.Int32)?displayProperty=nameWithType></li></ul>|

