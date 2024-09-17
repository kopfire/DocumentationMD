# Ac.ABS.Proxy.V1
1. [Физическое лицо](#Физическое-лицо)
	1. [Создание клиента в системе ИАБС  (Физ)](#Создание-клиента-в-системе-ИАБС--(Физ))
	2. [Изменение данных клиента в системе ИАБС (Физ)](#Изменение-данных-клиента-в-системе-ИАБС-(Физ))
	3. [Изменение данных клиента в системе ИАБС (Физ)](#Изменение-данных-клиента-в-системе-ИАБС-(Физ))
	4. [Идентификация данных клиента через систему ГЦП (Get Phisical) (Физ)](#Идентификация-данных-клиента-через-систему-ГЦП-(Get-Phisical)-(Физ))
	5. [Изменение данных клиента в системе ИАБС (Физ)](#Изменение-данных-клиента-в-системе-ИАБС-(Физ))
	6. [Изменение данных клиента в системе ИАБС (Физ)](#Изменение-данных-клиента-в-системе-ИАБС-(Физ))
## <a name="Физическое-лицо">Физическое лицо</a>
### <a name="Создание-клиента-в-системе-ИАБС--(Физ)">Создание клиента в системе ИАБС  (Физ)</a>
Endpoint ESB: **POST** **/1.0.0/create-customer** Формат **json**
#### Параметры запроса
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Headers)***|||
|requestId||string|
|Accept-Language|Accept-Language|string|
|***(HTTP-Body)***|||
|birthCountry|Страна рождения, Справочник №018 «Страны и территории»|string|
|codeFilial|Код филиала, Справочник №012 «Отделения банков РУз»|string|
|docType|Тип документа, Справочник № 008 «Виды удостоверяющих документов физического лица»|string|
|gender|Пол|string|
|residenceDistrict|Район проживания, Справочник №052 «Районы РУз»|string|
|firstName|Имя|string|
|mobilePhone|Мобильный телефон (998XXXXXXXXX)|string|
|residenceAddress|Адрес проживания|string|
|phone|Телефон|string|
|birthDate|Дата рождения|string|
|docExpireDate|Дата окончания действия документа|string|
|docIssueDate|Дата выдачи|string|
|docIssuePlace|Место выдачи документа|string|
|inn|ИНН клиента|string|
|maritalStatus|Семейное положение|string|
|middleName|Отчество|string|
|residenceCountry|Страна проживания, Справочник №018 «Страны и территории»|string|
|residenceRegion|Область проживания, Справочник №016 «Области РУз»|string|
|series|Серия паспорта|string|
|birthPlace|Место рождения|string|
|bxmCode|центр банковский услуг|string|
|citizenship|Гражданство, Справочник №018 «Страны и территории»|string|
|email|e-mail|string|
|lastName|Фамилия|string|
|number|Номер паспорта|string|
|pnfl|ПНФЛ|string|
#### Параметры ответа
##### HTTP-Code 200 OK
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Body)***|||
|code|Код результата|integer|
|msg|Сообщение|string|
|**responseBody**||object|
|responseBody.clientCode|Код клиента|string|
|responseBody.clientId|Уникальный идентификатор клиента|string|
##### HTTP-Code 400 Some of the required fields are not filled or invalid request body case.
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Body)***|||
|msg||string|
|oraMsg||string|
|code||integer|
##### HTTP-Code 401 Authorization error case.
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Body)***|||
|code||integer|
|msg||string|
|oraMsg||string|
##### HTTP-Code 403 Forbidden.
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Body)***|||
|msg||string|
|oraMsg||string|
|code||integer|
##### HTTP-Code 404 Resource Not Found.
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Body)***|||
|msg||string|
|oraMsg||string|
|code||integer|
##### HTTP-Code 500 Internal Error
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Body)***|||
|msg||string|
|oraMsg||string|
|code||integer|
### <a name="Изменение-данных-клиента-в-системе-ИАБС-(Физ)">Изменение данных клиента в системе ИАБС (Физ)</a>
Endpoint ESB: **GET** **/1.0.0/get-customer** Формат **json**
#### Параметры запроса
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Headers)***|||
|requestId||string|
|Accept-Language|Accept-Language|string|
|***(Query-params)***|||
|docType|Тип документа, Справочник № 008 «Виды удостоверяющих документов физического лица»|string|
|series|Серия документа клиента|string|
|number|Номер документа клиента|string|
|inn|ИНН клиента|string|
|pnfl|Персональный номер|string|
#### Параметры ответа
##### HTTP-Code 400 Some of the required fields are not filled or invalid request body case.
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Body)***|||
|code||integer|
|msg||string|
|oraMsg||string|
##### HTTP-Code 401 Authorization error case.
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Body)***|||
|code||integer|
|msg||string|
|oraMsg||string|
##### HTTP-Code 403 Forbidden.
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Body)***|||
|code||integer|
|msg||string|
|oraMsg||string|
##### HTTP-Code 404 Resource Not Found.
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Body)***|||
|code||integer|
|msg||string|
|oraMsg||string|
##### HTTP-Code 500 Internal Error
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Body)***|||
|msg||string|
|oraMsg||string|
|code||integer|
##### HTTP-Code 200 OK
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Body)***|||
|code|Код результата|integer|
|msg|Сообщение|string|
|**responseBody**||object|
|**responseBody.response**||array|
|responseBody.response[i].clientCode|Код клиента|string|
|responseBody.response[i].clientId|Уникальный идентификатор клиента|string|
|responseBody.response[i].birthPlace|Место рождения|string|
|responseBody.response[i].docIssueDate|Дата выдачи|string|
|responseBody.response[i].mobilePhone|Мобильный телефон (998XXXXXXXXX)|string|
|responseBody.response[i].residenceCountry|Страна проживания, Справочник №018 «Страны и территории»|string|
|responseBody.response[i].docType|Тип документа, Справочник № 008 «Виды удостоверяющих документов физического лица»|string|
|responseBody.response[i].residenceAddress|Адрес проживания|string|
|responseBody.response[i].series|Серия паспорта|string|
|responseBody.response[i].email|e-mail|string|
|responseBody.response[i].gender|Пол|string|
|responseBody.response[i].inn|ИНН клиента|string|
|responseBody.response[i].birthDate|Дата рождения|string|
|responseBody.response[i].codeFilial|Код филиала, Справочник №012 «Отделения банков РУз»|string|
|responseBody.response[i].docExpireDate|Дата окончания действия документа |string|
|responseBody.response[i].phone|Телефон|string|
|responseBody.response[i].lastName|Фамилия|string|
|responseBody.response[i].maritalStatus|Семейное положение|string|
|responseBody.response[i].middleName|Отчество|string|
|responseBody.response[i].status|Статус клиента|string|
|responseBody.response[i].citizenship|Гражданство, Справочник №018 «Страны и территории»|string|
|responseBody.response[i].firstName|Имя|string|
|responseBody.response[i].pnfl|Персональный номер|string|
|responseBody.response[i].residenceDistrict|Район проживания, Справочник №052 «Районы РУз»|string|
|responseBody.response[i].number|Номер паспорта|string|
|responseBody.response[i].residenceRegion|Область проживания, Справочник №016 «Области РУз»|string|
|responseBody.response[i].birthCountry|Страна рождения, Справочник №018 «Страны и территории»|string|
|responseBody.response[i].docIssuePlace|Место выдачи документа|string|
### <a name="Изменение-данных-клиента-в-системе-ИАБС-(Физ)">Изменение данных клиента в системе ИАБС (Физ)</a>
Endpoint ESB: **GET** **/1.0.0/get-customer/{clientId}** Формат **json**
#### Параметры запроса
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(Path-params)***|||
|clientId|Номер клиента|string|
|***(HTTP-Headers)***|||
|requestId||string|
|Accept-Language|Accept-Language|string|
#### Параметры ответа
##### HTTP-Code 404 Resource Not Found.
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Body)***|||
|code||integer|
|msg||string|
|oraMsg||string|
##### HTTP-Code 500 Internal Error
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Body)***|||
|code||integer|
|msg||string|
|oraMsg||string|
##### HTTP-Code 200 OK
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Body)***|||
|code|Код результата|integer|
|msg|Сообщение|string|
|**responseBody**||object|
|**responseBody.response**||array|
|responseBody.response[i].citizenship|Гражданство, Справочник №018 «Страны и территории»|string|
|responseBody.response[i].firstName|Имя|string|
|responseBody.response[i].lastName|Фамилия|string|
|responseBody.response[i].gender|Пол|string|
|responseBody.response[i].inn|ИНН клиента|string|
|responseBody.response[i].number|Номер паспорта|string|
|responseBody.response[i].phone|Телефон|string|
|responseBody.response[i].clientId|Уникальный идентификатор клиента|string|
|responseBody.response[i].residenceRegion|Область проживания, Справочник №016 «Области РУз»|string|
|responseBody.response[i].mobilePhone|Мобильный телефон (998XXXXXXXXX)|string|
|responseBody.response[i].residenceCountry|Страна проживания, Справочник №018 «Страны и территории»|string|
|responseBody.response[i].residenceDistrict|Район проживания, Справочник №052 «Районы РУз»|string|
|responseBody.response[i].birthCountry|Страна рождения, Справочник №018 «Страны и территории»|string|
|responseBody.response[i].docType|Тип документа, Справочник № 008 «Виды удостоверяющих документов физического лица»|string|
|responseBody.response[i].maritalStatus|Семейное положение|string|
|responseBody.response[i].clientCode|Код клиента|string|
|responseBody.response[i].series|Серия паспорта|string|
|responseBody.response[i].residenceAddress|Адрес проживания|string|
|responseBody.response[i].codeFilial|Код филиала, Справочник №012 «Отделения банков РУз»|string|
|responseBody.response[i].docExpireDate|Дата окончания действия документа |string|
|responseBody.response[i].email|e-mail|string|
|responseBody.response[i].middleName|Отчество|string|
|responseBody.response[i].birthPlace|Место рождения|string|
|responseBody.response[i].docIssuePlace|Место выдачи документа|string|
|responseBody.response[i].pnfl|Персональный номер|string|
|responseBody.response[i].birthDate|Дата рождения|string|
|responseBody.response[i].docIssueDate|Дата выдачи|string|
|responseBody.response[i].status|Статус клиента|string|
##### HTTP-Code 400 Some of the required fields are not filled or invalid request body case.
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Body)***|||
|code||integer|
|msg||string|
|oraMsg||string|
##### HTTP-Code 401 Authorization error case.
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Body)***|||
|code||integer|
|msg||string|
|oraMsg||string|
##### HTTP-Code 403 Forbidden.
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Body)***|||
|code||integer|
|msg||string|
|oraMsg||string|
### <a name="Идентификация-данных-клиента-через-систему-ГЦП-(Get-Phisical)-(Физ)">Идентификация данных клиента через систему ГЦП (Get Phisical) (Физ)</a>
Endpoint ESB: **GET** **/1.0.0/identify-customer** Формат **json**
#### Параметры запроса
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Headers)***|||
|requestId||string|
|Accept-Language|Accept-Language|string|
|***(Query-params)***|||
|series|Серия паспорта клиента|string|
|number|Номер паспорта клиента|string|
|inn|ИНН клиента|string|
|pinfl|Персональный номер|string|
|dateBirth|Дата рождения|string|
|agreement|Согласия клиента|string|
#### Параметры ответа
##### HTTP-Code 401 Authorization error case.
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Body)***|||
|code||integer|
|msg||string|
|oraMsg||string|
##### HTTP-Code 403 Forbidden.
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Body)***|||
|oraMsg||string|
|code||integer|
|msg||string|
##### HTTP-Code 404 Resource Not Found.
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Body)***|||
|code||integer|
|msg||string|
|oraMsg||string|
##### HTTP-Code 500 Internal Error
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Body)***|||
|msg||string|
|oraMsg||string|
|code||integer|
##### HTTP-Code 200 OK
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Body)***|||
|code|Код результата|integer|
|msg|Сообщение|string|
|**responseBody**||object|
|responseBody.nationalityName|Национальность - наименование|string|
|responseBody.residenceCountry|Страна проживания, Справочник №018 «Страны и территории»|string|
|responseBody.residenceRegion|Область проживания, Справочник №016 «Области РУз»|string|
|responseBody.docExpireDate|Дата окончания действия документа|string|
|responseBody.gender|Пол|string|
|responseBody.lastName|Фамилия|string|
|responseBody.residenceDistrict|Район проживания, Справочник №052 «Районы РУз»|string|
|responseBody.series|Серия паспорта|string|
|responseBody.middleName|Отчество|string|
|responseBody.number|Номер паспорта|string|
|responseBody.birthCountry|Страна рождения, Справочник №018 «Страны и территории»|string|
|responseBody.birthPlace|Место рождения|string|
|responseBody.docIssueDate|Дата выдачи|string|
|responseBody.docIssuePlace|Место выдачи документа|string|
|responseBody.firstName|Имя|string|
|responseBody.inn|ИНН клиента|string|
|responseBody.physicalState|Физическое состояние клиента|string|
|responseBody.residenceAddress|Адрес проживания|string|
|responseBody.birthDate|Дата рождения|string|
|responseBody.citizenship|Гражданство, Справочник №018 «Страны и территории»|string|
|responseBody.nationalityId|Национальность – код|string|
|responseBody.pnfl|Персональный номер|string|
##### HTTP-Code 400 Some of the required fields are not filled or invalid request body case.
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Body)***|||
|code||integer|
|msg||string|
|oraMsg||string|
### <a name="Изменение-данных-клиента-в-системе-ИАБС-(Физ)">Изменение данных клиента в системе ИАБС (Физ)</a>
Endpoint ESB: **PUT** **/1.0.0/update-customer** Формат **json**
#### Параметры запроса
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Headers)***|||
|requestId||string|
|Accept-Language|Accept-Language|string|
|***(HTTP-Body)***|||
|birthCountry|Страна рождения, Справочник №018 «Страны и территории»|string|
|birthDate|Дата рождения|string|
|birthPlace|Место рождения|string|
|docIssueDate|Дата выдачи|string|
|firstName|Имя|string|
|clientCode|Код клиента|string|
|clientId|Уникальный идентификатор клиента|string|
|gender|Пол|string|
|lastName|Фамилия|string|
|middleName|Отчество|string|
|number|Номер паспорта|string|
|pnfl|Персональный номер|string|
|series|Серия паспорта|string|
|citizenship|Гражданство, Справочник №018 «Страны и территории»|string|
|docExpireDate|Дата окончания действия документа|string|
|email|e-mail|string|
|maritalStatus|Семейное положение|string|
|mobilePhone|Мобильный телефон (998XXXXXXXXX)|string|
|phone|Телефон|string|
|residenceAddress|Адрес проживания|string|
|residenceDistrict|Район проживания, Справочник №052 «Районы РУз»|string|
|docIssuePlace|Место выдачи документа|string|
|docType|Тип документа, Справочник № 008 «Виды удостоверяющих документов физического лица»|string|
|inn|ИНН клиента|string|
|residenceCountry|Страна проживания, Справочник №018 «Страны и территории»|string|
|residenceRegion|Область проживания, Справочник №016 «Области РУз»|string|
#### Параметры ответа
##### HTTP-Code 200 OK
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Body)***|||
|code||integer|
|msg||string|
|oraMsg||string|
##### HTTP-Code 400 Some of the required fields are not filled or invalid request body case.
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Body)***|||
|code||integer|
|msg||string|
|oraMsg||string|
##### HTTP-Code 401 Authorization error case.
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Body)***|||
|oraMsg||string|
|code||integer|
|msg||string|
##### HTTP-Code 403 Forbidden.
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Body)***|||
|msg||string|
|oraMsg||string|
|code||integer|
##### HTTP-Code 404 Resource Not Found.
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Body)***|||
|code||integer|
|msg||string|
|oraMsg||string|
##### HTTP-Code 500 Internal Error
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Body)***|||
|code||integer|
|msg||string|
|oraMsg||string|
### <a name="Изменение-данных-клиента-в-системе-ИАБС-(Физ)">Изменение данных клиента в системе ИАБС (Физ)</a>
Endpoint ESB: **GET** **/1.0.0/check-customer** Формат **json**
#### Параметры запроса
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Headers)***|||
|requestId||string|
|Accept-Language|Accept-Language|string|
|***(Query-params)***|||
|clientId|Номер клиента|string|
|clientCode|Код клиента|string|
|series|Серия паспорта клиента|string|
|number|Номер паспорта клиента|string|
|codeFilial|Код филиала|string|
|name|Наименоваание клиента|string|
#### Параметры ответа
##### HTTP-Code 200 OK
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Body)***|||
|code|Код результата|integer|
|msg|Сообщение|string|
|**responseBody**||object|
|responseBody.response|(true,false)|string|
##### HTTP-Code 400 Some of the required fields are not filled or invalid request body case.
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Body)***|||
|code||integer|
|msg||string|
|oraMsg||string|
##### HTTP-Code 401 Authorization error case.
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Body)***|||
|code||integer|
|msg||string|
|oraMsg||string|
##### HTTP-Code 403 Forbidden.
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Body)***|||
|code||integer|
|msg||string|
|oraMsg||string|
##### HTTP-Code 404 Resource Not Found.
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Body)***|||
|oraMsg||string|
|code||integer|
|msg||string|
##### HTTP-Code 500 Internal Error
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Body)***|||
|code||integer|
|msg||string|
|oraMsg||string|
