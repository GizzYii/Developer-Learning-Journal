#PropTypes & Default Props

| English                                                      | Türkçe                                                               |
| ------------------------------------------------------------ | -------------------------------------------------------------------- |
| **PropTypes** provides runtime type checking for props.      | **PropTypes**, props’lar için çalışma zamanı tip kontrolü sağlar.    |
| PropTypes is useful when TypeScript is not used.             | TypeScript yoksa PropTypes çok faydalıdır.                           |
| PropTypes warnings appear in the console, not as errors.     | PropTypes uyarıları console’da çıkar, hata değildir.                 |
| `isRequired` marks a prop as mandatory.                      | `isRequired`, prop’un zorunlu olduğunu belirtir.                     |
| Missing required props triggers a warning.                   | Zorunlu prop gönderilmezse uyarı oluşur.                             |
| `oneOfType` allows multiple valid types for a prop.          | `oneOfType`, bir prop’un birden fazla tip almasına izin verir.       |
| `shape` validates the structure of an object prop.           | `shape`, obje prop’larının iç yapısını doğrular.                     |
| Nested object fields can also be marked as required.         | Obje içindeki alanlar da zorunlu yapılabilir.                        |
| **Default Props** provide fallback values for props.         | **Default Props**, prop gönderilmezse varsayılan değer atar.         |
| Default props prevent undefined values.                      | Default props undefined değerleri önler.                             |
| Modern React prefers default values via function parameters. | Modern React’te varsayılan değerler function parametresinde verilir. |
| Default props improve component stability.                   | Default props component kararlılığını artırır.                       |
